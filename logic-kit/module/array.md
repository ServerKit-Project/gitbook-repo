---
description: 배열 모듈
---

# Array

ServerKit에서 제공하는 Array 모듈 리스트는 아래와 같습니다.

* [at](array.md#array.at)
* [concat](array.md#array.concat)
* [includes](array.md#array.includes)
* [isArray](array.md#array.isarray)
* [join](array.md#array.join)
* [length](array.md#array.length)
* [push](array.md#array.push)
* [slice](array.md#array.slice)
* [updateatIndex](array.md#array.updateatindex)



***

## array.at

배열의 요소에 접근할 수 있는 모듈입니다.&#x20;

```javascript
const array = [5, 12, 8, 130];
const index = 2

const result = array.at(index)

console.log("result: ", result);
// result: 8
```

### param

`array: array<T>`

여러 요소들이 들어가 있는 배열입니다.



`index: number`

반환할 배열 요소의 0부터 시작하는 인덱스로, 정수로 변환됩니다. 음수일 경우 배열 끝부터 거슬러 셉니다.



### return

`result: <T>`

주어진 인덱스와 일치하는 배열의 요소입니다.



***

## array.concat

두 개 이상의 배열을 합치는데 사용되는 모듈로 새로운 배열을 만들어서 리턴합니다.

```javascript
const array_1 = ['a', 'b', 'c'];
const array_2 = ['d', 'e', 'f'];

const result = array_1.concat(array_2);

console.log("result: ", result);
// result: ["a", "b", "c", "d", "e", "f"]
```

### Param

`array_1: array<T>`

여러 요소가 합쳐져 있는 배열 1입니다.



`array_2: array<T>`

여러 요소가 합쳐져 있는 배열 2입니다.



### Return

`result: array<T>`

기존 배열 두개를 합쳐서 만들어진 새로운 배열입니다.



***

## array.includes

배열에 특정 값이 포함되어 있는지 체크할 수 있는 모듈입니다.

```javascript
const arr = ['cat', 'dog', 'bat'];
const valueToFind = 'dog';

const result = arr.includes(valueToFind);

console.log("result: ", result);
// result: true
```

### Param

`arr: array<T>`

여러개의 요소가 들어가 있는 배열입니다.



`valueToFind: <T>`

찾을 값입니다.



`fromIndex(optional): number`

검색을 시작할 0 기반 인덱스로, 정수로 변환됩니다.



### Return

`result: boolean`

배열 내에서 `valueToFind` 값이 발견되면 `true` 값이 전환됩니다.



***

## array.isArray

배열인지 확인하는 모듈입니다.

```javascript
const data = [1, 2, 4];

const result = Array.isArray(data);

console.log("result: ", result);
// result: true
```

### Param

`data: <T>`

배열인지 확인할 값입니다.



### Return

`result: boolean`

data가 Array라면 true, 그렇지 않다면 false를 반환합니다.



***

## array.join

배열의 요소를 문자열로 합쳐주는 모듈입니다.

```javascript
const array = ['Server', 'Kit'];
const separator = '-'

const result = array.join(separator);

console.log("result: ", result);
// result: Server-Kit
```

### Param

`array: array<T>`

여러 요소가 들어간 배열입니다.



`separator: string`

배열의 인접한 요소의 각 쌍을 구분하는 문자열입니다.



### Return

`result: string`

배열의 모든 요소들을 연결한 하나의 문자열을 반환합니다.&#x20;

{% hint style="info" %}
만약 array.length가 0일 경우 빈 문자열일 반환됩니다.
{% endhint %}



***

## array.length

배열의 길이를 반환하는 모듈입니다.

```javascript
const array = ['Server', 'Kit'];

const result = array.length;

console.log("result: ", result);
// result: 2
```

### Param

`array: array<T>`

여러 요소가 있는 배열입니다.



### Return

`result: number`

배열의 길이입니다.

{% hint style="info" %}
요소가 없는 빈 배열일 경우 0으로 반환됩니다.
{% endhint %}



***

## array.push

배열의 끝에 요소를 추가할 수 있는 모듈입니다.

```javascript
const array = ['Server', 'Kit'];
const item = '!';

const result = array.push(item);

console.log("result: ", result);
// result: ['Server', 'Kit', '!']
```

### Param

`array: array<T>`

여러 요소가 있는 배열입니다.



`item: <T>`

배열의 끝에 추가할 요소입니다.



### Return

`result: array<T>`

item이 끝에 추가된 배열입니다.



***

## array.slice

배열의 특정 범위의 요소를 잘라내어 추출한 결과를 새로운 배열로 반환하는 모듈입니다.

```javascript
const array = ['Hello', 'Server', 'Kit', 'World'];
const begin = 1;
const end = 3;

const result = array.slice(begin, end);

console.log("result: ", result);
// result: ['Server', 'Kit']
```

### Param

`array: array<T>`

여러 요소가 있는 배열입니다.



`begin: number`

추출 시작점으로 0부터 시작하는 인덱스를 의미합니다.



`end(optional): number`

추출 종료점입니다.

{% hint style="info" %}
end를 생략할 경우 배열 끝까지 추출됩니다.\
end 값이 배열의 길이보다 크다면, 배열의 끝가지 추출합니다.
{% endhint %}



### Return

`result: array<T>`

추출한 요소를 포함한 새로운 배열입니다.



***

## array.updateAtIndex

입력한 index에 있는 요소를 입력한 value 값으로 바꾸는 모듈입니다.

```javascript
const array = ['Server', 'Kit', '?'];
const index = 2;
const value = '!';

array[index] = value;
const result = array;

console.log("result: ", result);
// result: ['Server', 'Kit', '!']
```

### Param

`array: array<T>`

여러 요소가 있는 배열입니다.



`index: number`

0부터 시작하는 요소를 바꿀 자릿값입니다.



`value: <T>`

바꿀 요소입니다.



### Return

`result: array<T>`

바뀐 배열입니다.





