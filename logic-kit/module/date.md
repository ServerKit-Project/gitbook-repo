---
description: 날짜 모듈
---

# Date

ServerKit에서 제공하는 Date 모듈 리스트입니다.

* [getCron](date.md#date.getcron)
* [getDate](date.md#date.getdate)
* [getDay](date.md#date.getday)
* [getFullYear](date.md#date.getfullyear)
* [getHours](date.md#date.gethours)
* [getMilliseconds](date.md#date.getmilliseconds)
* [getMinutes](date.md#date.getminutes)
* [newDate](date.md#date.newdate)
* [nowDate](date.md#date.nowdate)
* [setDate](date.md#date.setdate)
* [setHours](date.md#date.sethours)
* [setMilliseconds](date.md#date.setmilliseconds)
* [setMinutes](date.md#date.setminutes)
* [setMonth](date.md#date.setmonth)
* [setSeconds](date.md#date.setseconds)
* [setYear](date.md#date.setyear)



***

## date.getCron

date을 cron으로 변환시켜줍니다.

```javascript
const inputDate = new Date();

const dayOfMonth = inputDate.getDate();
const month = inputDate.getMonth() + 1;
const dayofWeek = inputDate.getDay();
const hour = inputDate.getHours();
const minute = inputDate.getMinutes();

const result = `${minute} ${hour} ${dayOfMonth} ${month} ${dayOfWeek}`;

console.log('result: ', result);
// result: 11 24 22 2
```

### param

`inputDate: date`

cron 형식으로 변환시켜줄 date입니다.



### return

`result: string`

cron 형식이 된 요소입니다.



***

## date.getDate

주어진 날짜의 일(1\~31)을 반환합니다.

```javascript
const date = new Date('August 19, 1975 23:15:30');

const result = date.getDate();

console.log('result: ', result);
// result: 19
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜의 일에 해당하는 1 이상 31 이하의 정수입니다.



***

## date.getDay

주어진 날짜의 요일을 반환합니다. 0은 일요일을 나타냅니다.

```javascript
const date = new Date('August 19, 1975 23:15:30');

const result = date.getDay();

console.log('result: ', result);
// result: 2
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜의 요일에 해당하는 0 이상 6 이하의 정수입니다. 0은 일요일, 1은 월요일, 6은 토요일입니다.



***

## date.getFullYear

주어진 날짜의 연도를 반환합니다.

```javascript
const date = new Date('August 19, 1975 23:15:30');

const result = date.getFullYear();

console.log('result: ', result);
// result: 1975
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜의 연도에 해당하는 숫자입니다.



***

## date.getHours

주어진 날짜의 시를 반환합니다.&#x20;

```javascript
const date = new Date('March 13, 08 04:20')

const result = date.getHours();

console.log('result: ', result);
// result: 4
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜에 해당하는 시입니다. 0에서 23 사이의 정수입니다.



***

## date.getMilliseconds

밀리초를 반환합니다.

```javascript
const date = new Date('March 13, 08 04:20')

const result = date.getMilliseconds(999);

console.log('result: ', result);
// result: 999 
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜의 밀리초입니다. 0에서 999 사이의 정수입니다.



***

## date.getMinutes

밀리초를 반환합니다.

```javascript
const date = new Date('March 13, 08 04:20')

const result = date.getMinutes(999);

console.log('result: ', result);
// result: 20
```

### param

`date: date`

확인하고자 하는 날짜입니다.



### return

`result: number`

주어진 날짜의 분입니다. 0에서 59 사이의 정수입니다.



***

## date.newDate

date를 생성합니다.

```javascript
const value = 'March 13, 08 04:20'

const result = new Date(value);

console.log('result: ', result);
// result: 2008-03-12T19:20:00.000Z
```

### param

`value: string`

date로 바꾸고 싶은 문자열입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.nowDate

현재 date을 생성합니다.

```javascript
const result = new Date()

console.log('result: ', result);
// result: 2024-02-22T02:42:49.914Z
```

### return

`result: date`

현재 날짜로 생성된 date입니다.



***

## date.setDate

월의 시작 부분을 기준으로 date을 변경합니다.

```javascript
const date = '2008-03-12T19:20:00.000Z'
const dateVale = 2

const result = date.setDate(dateVale);

console.log('result: ', result);
// result: 2008-03-14T19:20:00.000Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`dateValue: number`

월의 일을 나타내는 정수입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.setHours

date의 시간을 변경합니다.

```javascript
const date = '2008-03-12T19:20:00.000Z'
const hoursValue = 1

const result = date.setHours(dateVale);

console.log('result: ', result);
// result: 2008-03-12T20:20:00.000Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`hoursValue: number`

시를 나타내는 0에서 23 사이의 정수입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.setMilliseconds

밀리 초를 변경합니다.

```javascript
const date = '1997-02-22T03:16:04.484Z'
const millisecondsValue = 100

const result = date.setMilliseconds(millisecondsValue);

console.log('result: ', result);
// result: 1997-02-22T03:16:04.100Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`millisecondsValue: number`

밀리 초를 나타내는 0에서 999 사이의 숫자입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.setMinutes

분을 변경합니다.

```javascript
const date = '2008-03-12T19:20:00.000Z'
const minutesValue = 20

const result = date.setMinutes(minutesValue);

console.log('result: ', result);
// result: 2008-03-12T19:40:00.000Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`minutesValue: number`

분을 나타내는 0에서 59 사이의 정수입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.setMonth

달을 변경합니다.

```javascript
const date = '2008-03-12T19:20:00.000Z'
const monthValue = 0

const result = date.setMonth(monthValue);

console.log('result: ', result);
// result: 2008-01-12T19:20:00.000Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`monthValue: number`

달을 나타내는 0 기반 정수입니다. 0은 1월, 11은 12월, -1은 전년도의 12월, 12은 다음해의 1월을 나타냅니다.&#x20;



### return

`result: date`

바뀐 date입니다.



***

## date.setSeconds

초를 변경합니다.

```javascript
const date = 'August 19, 1975 23:15:30'
const secondsValue = 42

const result = date.setSeconds(secondsValue);

console.log('result: ', result);
// result: Sat Apr 19 1975 23:15:42 GMT+0100 (CET)
```

### param

`date: date`

변경하고 싶은 date입니다.



`secondsValue: number`

초를 나타내는 0에서 59 사이의 정수입니다.



### return

`result: date`

바뀐 date입니다.



***

## date.setYear

연도를 변경합니다.

```javascript
const date = '2024-02-22T03:16:04.484Z'
const yearValue = 1997

const result = date.setFullYear(secondsValue);

console.log('result: ', result);
// result: 1997-02-22T03:16:04.484Z
```

### param

`date: date`

변경하고 싶은 date입니다.



`yearValue: number`

연도의 숫자 값을 지정하는 정수압니다.



### return

`result: date`

바뀐 date입니다.







