## naver
### Parameters
- serviceId: string
- from: string
- content: string
- to: string
- accessKey: string
- signature: string
- timestamp: string

### Return
- result: object

--------------------------------------------
## naverTimestamp
### Parameters
- No Param
### Return
- result: string

--------------------------------------------
## sejongtelecom
### Parameters
- callback: string
- contents: string
- receiverTelNo: string
- userKey: string
- resellerCode: string
- sejongApiKey: string
- url: string
- title: string

### Return
- result: number

--------------------------------------------
## naverSignature
### Parameters
- method: string
- url: string
- timestamp: string
- accessKey: string
- secretKey: string

### Return
- result: string

--------------------------------------------
## sejongtelecomManyTime
### Parameters
- callback: string
- contents: Array<string>

### Return
- No Return
--------------------------------------------
## sejongtelecomMany
### Parameters
- callback: string
- contents: Array<string>

### Return
- result: Array<string>

--------------------------------------------
## sejongtelecomTime
### Parameters
- callback: string
- contents: string
- receiverTelNo: string
- userKey: string
- resellerCode: string
- sejongApiKey: string
- url: string
- time: date
- title: string
- checkInId: string

### Return
- No Return
--------------------------------------------
