---
description: 2차 인증 모듈
---

# Auth

ServerKit에서 제공하는 Auth 모듈 리스트는 아래와 같습니다.

* [signUp2fSave](auth.md#auth.signup2fsave)
* [signUp2faCheck](auth.md#auth.signup2facheck)
* [createMFASession](auth.md#auth.createmfasession)
* [validateMFASession](auth.md#auth.validatemfasession)



***

## auth.signUp2fSave

회원가입 시 사용하는 모듈로 인증번호를 저장합니다. [createMFASession](auth.md#auth.createmfasession)과의 차이점은 토큰을 사용하지 않는 것과 userId가 필요없다는 것입니다.

```javascript
const phonNumber = '000-0000-0000';
const verificationCode = 'k2lsdj0';
const TTL = '1000';

// Redis에 저장합니다.
const redis = require('redis');
const client = redis.createClient();

client.connect();

client.on('connect', () => {});
client.one('error', () => {});

client.on('ready', () => {
    client
        .multi()
        .hSet(`code:${phonNumber}`, verificationCode)
        .expire(`code:${phonNumber}`, TTL)
        .exec()
        .then(() => { console.log('result: ', 200) })
        .catch(() => { console.log('result: ', 400) })
});

// 성공했을 경우 result: 200
// 실패했을 경우 result: 400
```

### param

`phoneNumber: string`

유일한 key 값입니다. 향후 [signUp2faCheck](auth.md#auth.signup2facheck) 모듈을 사용하여 인증번호를 확인할 때 사용됩니다.



`verificationCode: string`

저장할 인증번호입니다. [랜덤 모듈](random.md)을 사용하면 좋습니다.



`TTL: number`

유효시간입니다. 초단위이며 60초에 1분이며 300을 넣으면 5분이 됩니다.



### return

`result: number`

성공할 경우 200, 실패할 경우 에러 문구가 나옵니다.



***

## auth.signUp2faCheck

[signUp2faSave](auth.md#auth.signup2fsave)을 이용하여 회원가입시 인증번호를 저장했다면 사용자가 입력한 인증번호와 맞는지 대조 후 결과값을 반환하는 모듈입니다.

```javascript
const verificationCode = 'k2lsdj0';
const phoneNumber = '000-0000-0000';

// Redis에 조회합니다.
const redis = require('redis');
const client = redis.createClient();

client.connect();

client.on('connect', () => {});
client.one('error', () => {});

client.on('ready', async () => {
    const redisAuthNumber = await client.hGet(`code:${phonNumber}`);
    
    if(redisAuthNumber === verificationCode) {
        console.log('result: true')
    } else {
        console.log('result: fail')
    }
    
    client.quit();
});
// 성공했을 경우 result: true
// 실패했을 경우 result: fail
```

### param

`verificationCode: string`

[signUp2faSave](auth.md#auth.signup2fsave)서 저장한 인증코드입니다.&#x20;



`phoneNumber: string`

[signUp2faSave](auth.md#auth.signup2fsave)에서 저장한 유일한 key 값입니다.



### return

`result:  boolean`

인증번호 인증이 성공한 경우 true가 나오고 실패한 경우 fail이 나옵니다.



***

## auth.createMFASession

로그인 시 사용되는 모듈로 인증번호를 저장합니다. [signUp2faSave](auth.md#auth.signup2fsave)와의 차이점은 토큰을 사용한다는 것과 userId가 필요합니다.

```javascript
const userGroupId = 'userGroup1';
const verificationCode = 'dk92kdks';
const userId = 'userId1';
const TTL = 300;

// Redis에 저장합니다.
const redis = require('redis');
const client = redis.createClient();

client.connect();

client.on('connect', () => {});
client.one('error', () => {});

client.on('ready', () => {
    try {
        await client.hSet(`code:${userId}`, verificationCode);
        await client.expirte(`code:${userId}`, TTL);
        console.log(`result:`, { sessionId : `code:${userId}` })
    } catch (e) {
        console.log(`result: ${e}`);
    }
});
// 성공했을 경우 result: { sessionI: 'code:userId1' }
// 실패했을 경우 result: 에러 객체
```

### param

`userGroupId: string`

[UserKit에서 만든 User Group](../../user-kit/user-group.md) Id입니다.



`verificationCode: string`

로그인 인증 번호입니다.



`userId: string`

로그인을 시도한 user의 Id입니다.



`TTL: number`

유효시간입니다. 초단위이며 60초에 1분이며 300을 넣으면 5분이 됩니다.



### return

`result: object`

sessionId가 담겨져 있는 결과값입니다.



***

## auth.validateMFASession

로그인 시 사용되는 모듈로 인증번호를 인증합니다.

```javascript
const userGroupId = 'userGroup1';
const verificationCode = 'dk92kdks';
const sessionId = 'code:userId1';

// Redis에 저장합니다.
const redis = require('redis');
const client = redis.createClient();

client.connect();

client.on('connect', () => {});
client.one('error', () => {});

client.on('ready', async () => {
    const redisVerificationCode = await client.hGet(sessionId);
    if(!redisVerificationCode) {
        console.log('result: 400');
    }
    
    // userKit 통신을 통해 Token 발급
    const issueTokenResult = await axios
        .post('userkit-api');
        .catch((e) => { console.log('result:', e) }
    console.log('result: { token: issueTokenResult } 
});
// 성공했을 경우 result: { code: { token: 'serverkit' } }
// 실패했을 경우 result: 에러 객체
```

### param

`userGroupId: string`

[UserKit에서 만든 User Group](../../user-kit/user-group.md) Id입니다.



`verificationCode: string`

로그인 인증 번호입니다.



`sessionId: string`

[createMFASession](auth.md#auth.createmfasession)의 반환값입니다.



### return

`result: object`

UserKit에서 발급한 token이 담겨져 있는 반환값입니다.







