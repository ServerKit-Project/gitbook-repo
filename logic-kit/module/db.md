## delete
### Parameters
- database: database
- query: queryObject

### Return
- result: number

--------------------------------------------
## deleteUser
### Parameters
- userGroupId: string
- userId: string

### Return
- result: number

--------------------------------------------
## getFind
### Parameters
- database: database
- query: queryObject
- page: number
- length: number
- orderCreatedAt: number

### Return
- result: array (T)

--------------------------------------------
## getFindAdv
### Parameters
- database: database
- query: queryObject
- page: number
- length: number
- orderCreatedAt: number
- sort: object

### Return
- result: object

--------------------------------------------
## getFindCount
### Parameters
- database: database
- query: queryObject
- page: number
- length: number
- orderCreatedAt: number
- sort: object

### Return
- result: number

--------------------------------------------
## getFindUserSearchUserId
### Parameters
- userGroupId: string
- word: string

### Return
- userId: string
- userGroupId: string

--------------------------------------------
## getFindUser
### Parameters
- userGroupId: string
- userId: string

### Return
- result: object

--------------------------------------------
## getUserByToken
### Parameters
- userGroupId: string
- token: string

### Return
- result: object

--------------------------------------------
## getFindUserSearch
### Parameters
- userGroupId: string
- word: string
- pageNumber: number
- pageSize: number

### Return
- result: totalUserData

--------------------------------------------
## postCreateBulkCSV
### Parameters
- database: database
- data: string

### Return
- result: number

--------------------------------------------
## postCreateBulkXML
### Parameters
- database: database
- data: string

### Return
- result: number

--------------------------------------------
## postCreateBulkJSON
### Parameters
- database: database
- data: string

### Return
- result: number

--------------------------------------------
## postCreateMany
### Parameters
- database: database
- data: array (T)

### Return
- result: number

--------------------------------------------
## postCreateUser
### Parameters
- data: object

### Return
- result: number

--------------------------------------------
## postCreate
### Parameters
- database: database
- query: queryObject

### Return
- result: number

--------------------------------------------
## putUpdate
### Parameters
- database: database
- query: queryObject
- action: action (T)

### Return
- result: number

--------------------------------------------
## updateCustomValue
### Parameters
- userGroupId: string
- userId: string
- keyValueObject: object

### Return
- result: object

--------------------------------------------
## putUpdateManyTime
### Parameters
- database: database
- query: queryObject
- time: Array<date>
- checkInId: Array<string>
- value: Array<string>
- action: action (T)

### Return
No Return
--------------------------------------------
## putUpdateUser
### Parameters
- data: object

### Return
- result: number

--------------------------------------------
## putUpdateTime
### Parameters
- database: database
- query: queryObject
- time: date
- checkInId: string
- action: action (T)

### Return
No Return
--------------------------------------------
