---
description: 암호화 모듈
---

# Bcrypt

SeverKit에서 제공하는 Bcrypt 모듈은 아래와 같습니다.

* [genSaltSync](bcrypt.md#bcrypt.gensaltsync)
* [hashSync](bcrypt.md#bcrypt.hashsync)
* [compareSync](bcrypt.md#bcrypt.comparesync)



***

## bcrypt.genSaltSync

비밀번호 보안을 강화하기 위해 비밀번호에 추가되는 무작위 문자열을 반환하는 모듈입니다. [hashSync 모듈](bcrypt.md#bcrypt.hashsync)과 함께 사용하면 좋습니다.

```javascript
const round = 10;

const result = bcrypt.genSaltSync(round);

console.log("result: ", result);
// result: $2b$10$2UixIJ4....
```

### param

`round: number`

salt를 생성할 때 사용되는 작업의 복잡성을 결정합니다. 높을 수록 salt를 생성하는데 더 많은 시간과 자원이 필요하며, 이는 비밀번호 해싱 과정을 더 안전하게 만듭니다.



### return

`result: string`

무작위 문자열입니다.



## bcrypt.hashSync

암호화 하고 싶은 요소를 hash 값으로 바꿔주는 모듈입니다.

```javascript
const data = 'abc';
const salt = bcrypt.genSaltSync(10);

const result = bcrypt.hashSync(data, salt);

console.log("result: ", result);
// result: $2b$10$...
```

### param

`data: string`

암호화 하고 싶은 요소입니다.



`salt: number`

[genSaltSync 모듈](bcrypt.md#bcrypt.gensaltsync)을 사용한 무작위 문자열입니다.



### return

`result: string`

암호화 하고 싶은 data와 salt가 결합하여 해싱한 값입니다.



***

## bcrypt.compareSync

[hashSync 모듈](bcrypt.md#bcrypt.hashsync)을 이용해 암호화한 해쉬값과 특정 요소가 동일한지 비교하는 모듈입니다.

```javascript
const data = 'abc';
const encryptedData = '$2b$10$...';

const result = bcrypt.compareSync(data, encryptedData);

console.log("result: ", result);
// 성공했을 경우 result: true;
// 실패했을 경우 result: fail;
```

### param

`data: string`

비교할 요소입니다.



`encryptedData: string`

암호화 된 요소입니다.



### return

`result: boolean`

비교할 요소와 암호화 된 요소가 같을 경우 true가 반환되고 아닐 경우 fail이 반환됩니다.





