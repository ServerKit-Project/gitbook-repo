---
description: 날짜 모듈
---

# Dayjs

### dayjs

#### Parameters

* date: string

#### Return

* result: date

***

### add

#### Parameters

* No Param

#### Return

* No Return

***

### diffDay

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffMillisecond

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffQuarter

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffMinute

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffMonth

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffHour

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### format

#### Parameters

* date: date
* form: string

#### Return

* result: string

***

### diffWeek

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### diffYear

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### getDay

#### Parameters

* date: date

#### Return

* result: number

***

### diffSecond

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: number

***

### getDate

#### Parameters

* date: date

#### Return

* result: number

***

### getHour

#### Parameters

* date: date

#### Return

* result: number

***

### getMillisecond

#### Parameters

* date: date

#### Return

* result: number

***

### getMonth

#### Parameters

* date: date

#### Return

* result: number

***

### getSecond

#### Parameters

* date: date

#### Return

* result: number

***

### isBefore

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: boolean

***

### isAfter

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: boolean

***

### getYear

#### Parameters

* date: date

#### Return

* result: number

***

### isSame

#### Parameters

* startDate: date
* endDate: date

#### Return

* result: boolean

***

### setDate

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### isBetween

#### Parameters

* startDate: date
* someDate: date
* endDate: date

#### Return

* result: boolean

***

### setHour

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setMillsecond

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setDay

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setMonth

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setMinute

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setSecond

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### setYear

#### Parameters

* date: date
* value: number

#### Return

* result: date

***

### timeAsiaSeoul

#### Parameters

* date: date

#### Return

* result: date

***

### timeOther

#### Parameters

* date: date
* region: date

#### Return

* result: date

***

### subtract

#### Parameters

* No Param

#### Return

* No Return

***

Serverkit에서 제공하는 Dayjs 모듈입니다.

* [add](dayjs.md#add)
* [dayjs](dayjs.md#dayjs)
* [diffDay](dayjs.md#diffday)
* [diffHour](dayjs.md#diffhour)
* [diffMillisecond](dayjs.md#diffmillisecond)
* [diffMinute](dayjs.md#diffminute)
* [diffMonth](dayjs.md#diffmonth)
* [diffQuarter](dayjs.md#diffquarter)
* [diffSecond](dayjs.md#diffsecond)
* [diffWeek](dayjs.md#diffweek)
* [diffYear](dayjs.md#diffyear)
* [format](dayjs.md#format)
* [getDate](dayjs.md#getdate)
* [getDay](dayjs.md#getday)
* [getHour](dayjs.md#gethour)
* [getMillisecond](dayjs.md#getmillisecond)
* [getMonth](dayjs.md#getmonth)
* [getSecond](dayjs.md#getsecond)
* [getYear](dayjs.md#getyear)
* [isAfter](dayjs.md#isafter)
* [isBefore](dayjs.md#isbefore)
* [isBetween](dayjs.md#isbetween)
* [isSame](dayjs.md#issame)
* [setDate](dayjs.md#setdate)
* [setDay](dayjs.md#setday)
* [setHour](dayjs.md#sethour)
* [setMillisecond](dayjs.md#setmillisecond)
* [setMinute](dayjs.md#setminute)
* [setMonth](dayjs.md#setmonth)
* [setSecond](dayjs.md#setsecond)
* [setYear](dayjs.md#setyear)
* [subtract](dayjs.md#subtract)
* [timeAsiaSeoul](dayjs.md#timeasiaseoul)
* [timeOther](dayjs.md#timeother)



***



## dayjs.add

날짜 및 시간을 더합니다.

```javascript
const date = dayjs();
const number = 1;
const day = 'day';

const result = date.add(number,day);
```

### param

`date: date`

cron 형식으로 변환시켜줄 date입니다.



`number: number`

기존 date에 더할 숫자입니다.



`day: string`

어떤 유형의 날짜를 바뀔 지 아래 표를 참고하여 기입합니다.

<table><thead><tr><th width="275">단위</th><th>설명</th></tr></thead><tbody><tr><td>day</td><td>일</td></tr><tr><td>week</td><td>주</td></tr><tr><td>month</td><td>월</td></tr><tr><td>quarter</td><td>분기</td></tr><tr><td>year</td><td>년도</td></tr><tr><td>hour</td><td>시간</td></tr><tr><td>minute</td><td>분</td></tr><tr><td>second</td><td>초</td></tr><tr><td>millisecond</td><td>밀리초</td></tr></tbody></table>



### return

`result: date`

추가된 Date입니다.



***

## dayjs

날짜를 반환합니다.&#x20;



```javascript
const date = '2019-01'
const result = dayjs(date)
// 2019-01-01T00:00:00+00:00
```

### param

`date(optional): string`

전환할 date.



### return

`result: date`

나온 date.







## diffDay

## diffHour

## diffMillisecond

## diffMinute

## diffMonth

## diffQuarter

## diffSecond

## diffWeek

## diffYear

## format

## getDate

## getDay

## getHour

## getMillisecond

## getMonth

## getSecond

## getYear

## isAfter

## isBefore

## isBetween

## isSame

## setDate

## setDay

## setHour

## setMillisecond

## setMinute

## setMonth

## setSecond

## setYear

## subtract

## timeAsiaSeoul

## timeOther









