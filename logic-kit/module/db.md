# DB

ServerKit에서 제공하는 DB 모듈 리스트입니다.

* db.delete.ts
* db.deleteUser.js
* db.getFind.ts
* db.getFindAdv.js
* db.getFindCount.js
* db.getFindUser.js
* db.getFindUserSearch.js
* db.getFindUserSearchUserId.js
* db.getUserByToken.js
* db.postCreate.ts
* db.postCreateBulkCSV.js
* db.postCreateBulkJSON.js
* db.postCreateBulkXML.js
* db.postCreateMany.js
* db.postCreateUser.js
* db.putUpdate.ts
* db.putUpdateManyTime.js
* db.putUpdateTime.js
* db.putUpdateUser.js
* db.updateCustomValue.js

***

## db.delete 모듈

### Param:

* **database (database)**: 삭제 작업을 수행할 데이터베이스입니다.
* **query (queryObject)**: 삭제를 수행할 쿼리 객체입니다.

### Return:

* **result (number)**: 삭제 작업의 결과로, 성공 시 100, 실패 시 에러 코드를 반환합니다.

이 모듈은 데이터베이스에서 특정 데이터를 삭제합니다. `axios`를 사용하여 서버에 삭제 요청을 비동기적으로 보냅니다. 요청이 성공하면, `success` 콜백이 호출되고, 실패하면 `fail` 콜백이 호출됩니다. `action` 함수 내에서 처리된 응답이나 에러에 따라 적절한 콜백을 실행합니다.

***

## db.deleteUser 모듈

### Param:

* **userGroupId (string)**: 사용자가 속한 그룹의 식별자입니다.
* **userId (string)**: 삭제할 사용자의 식별자입니다.

### Return:

* **result (number)**: 요청 처리 결과입니다. 성공적인 삭제 시에는 1, 그렇지 않으면 0 또는 오류 코드가 될 수 있습니다.

이 모듈은 `userGroupId`와 `userId`를 사용하여 특정 사용자를 데이터베이스에서 삭제합니다. `axios` 라이브러리를 사용해 HTTP DELETE 요청을 서버에 비동기적으로 보냅니다. 요청이 성공하면 `success` 콜백이 호출되며, 요청이 실패하면 `fail` 콜백이 호출됩니다. `action` 함수는 서버의 응답에 따라 적절한 콜백을 실행하며, 에러가 발생한 경우 에러 정보를 `result`에 할당합니다.

***

## db.getFind 모듈

### Param:

* **database (database)**: 조회할 데이터베이스입니다.
* **query (queryObject)**: 조회에 사용할 쿼리 객체입니다.
* **page (number)**: 조회할 페이지 번호입니다. 기본값은 1입니다.
* **length (number)**: 페이지당 결과 수입니다. 기본값은 10입니다.
* **orderCreatedAt (number)**: 생성 날짜 기준으로 정렬 방향을 지정합니다. 1은 오름차순, -1은 내림차순을 나타냅니다.

### Return:

* **result (array of T)**: 조회된 데이터의 배열입니다. `T`는 템플릿 시그니처로, 반환될 객체의 타입을 나타냅니다.

이 모듈은 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터를 조회합니다. `axios` 라이브러리를 사용해 HTTP POST 요청을 서버에 비동기적으로 보냅니다. 요청이 성공하면 `success` 콜백이 호출되고, 실패하면 `fail` 콜백이 호출됩니다. `action` 함수는 서버로부터의 응답에 따라 결과 배열을 `result`에 할당하고 적절한 콜백을 실행합니다.

***

## db.getFindAdv 모듈

### Param:

* **database (database)**: 조회할 데이터베이스입니다.
* **query (queryObject)**: 조회에 사용할 쿼리 객체입니다.
* **page (number)**: 조회할 페이지 번호입니다. 기본값은 1입니다.
* **length (number)**: 페이지당 결과 수입니다. 기본값은 10입니다.
* **orderCreatedAt (number)**: 생성 날짜 기준으로 정렬 방향을 지정합니다. 1은 오름차순, -1은 내림차순을 나타냅니다.
* **sort (object)**: 정렬 기준을 나타내는 객체입니다.

### Return:

* **result (object)**: 조회된 데이터와 추가 정보를 포함하는 객체입니다.

이 모듈은 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터를 고급 옵션과 함께 조회합니다. `axios` 라이브러리를 사용해 HTTP POST 요청을 비동기적으로 서버에 보냅니다. 요청이 성공하면 `success` 콜백이 호출되고, 실패하면 `fail` 콜백이 호출됩니다. `action` 함수는 서버로부터의 응답에 따라 결과 객체를 `result`에 할당하고 적절한 콜백을 실행합니다.

***

## db.getFindCount 모듈

### Param:

* **database (database)**: 조회할 데이터베이스입니다.
* **query (queryObject)**: 조회에 사용할 쿼리 객체입니다.
* **page (number)**: 조회할 페이지 번호입니다. 기본값은 1입니다.
* **length (number)**: 페이지당 결과 수입니다. 기본값은 10입니다.
* **orderCreatedAt (number)**: 생성 날짜 기준으로 정렬 방향을 지정합니다. 1은 오름차순, -1은 내림차순을 나타냅니다.
* **sort (object)**: 정렬 기준을 나타내는 객체입니다.

### Return:

* **result (number)**: 조회된 데이터의 총 개수입니다.

이 모듈은 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터의 총 개수를 조회합니다. `axios` 라이브러리를 사용해 HTTP POST 요청을 비동기적으로 서버에 보냅니다. 요청이 성공하면 조회된 데이터의 총 개수를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 `fail` 콜백을 호출합니다. `action` 함수는 서버로부터의 응답을 처리하여 `result`에 데이터의 총 개수를 할당하고 적절한 콜백을 실행합니다.

***

## db.getFindUser 모듈

### Param:

* **userGroupId (string)**: 조회할 유저가 속한 그룹의 ID입니다.
* **userId (string)**: 조회할 유저의 ID입니다.

### Return:

* **result (object)**: 조회된 유저 정보를 포함하는 객체입니다.

이 모듈은 지정된 `userGroupId`와 `userId`를 사용하여 유저 정보를 조회합니다. `axios` 라이브러리를 사용해 HTTP GET 요청을 서버에 비동기적으로 보냅니다. 요청이 성공하면 조회된 유저 정보를 `result`에 할당하고 `success` 콜백을 호출합니다. 만약 요청이 실패하면, 오류 응답을 `result`에 할당하고 `fail` 콜백을 호출합니다.

***

## db.getFindUserSearch 모듈

### Param:

* **userGroupId (string)**: 검색할 유저가 속한 그룹의 ID입니다.
* **word (string)**: 검색어입니다.
* **pageNumber (number)**: 페이지 번호입니다.
* **pageSize (number)**: 페이지당 유저 수입니다.

### Return:

* **result (totalUserData)**: 검색된 유저 데이터와 관련 총 정보를 포함하는 객체입니다.

이 모듈은 주어진 `userGroupId` 내에서 `word`를 포함하는 유저를 검색합니다. 페이지네이션은 `pageNumber`와 `pageSize` 매개변수를 통해 제어됩니다. `axios` 라이브러리를 이용해 서버에 비동기적으로 HTTP GET 요청을 보내고, 성공적으로 유저 데이터를 검색하면 `success` 콜백을 호출하고, 오류가 발생하면 `fail` 콜백을 호출합니다.

***

## db.getFindUserSearchUserId 모듈

### Param:

* **userGroupId (string)**: 검색할 유저 그룹 ID입니다.
* **word (string)**: 검색어입니다.

### Return:

* **userId (string)**: 검색된 유저의 ID입니다.
* **userGroupId (string)**: 검색된 유저가 속한 그룹의 ID입니다.

이 모듈은 특정 그룹에 속한 유저 중 검색어에 맞는 유저의 ID와 그룹 ID를 조회합니다. `axios` 라이브러리를 이용해 서버에 비동기적으로 HTTP GET 요청을 보내고, 성공적으로 유저 데이터를 검색하면 반환값에 유저 ID와 그룹 ID를 설정하고 `success` 콜백을 호출합니다. 요청이 실패하면 오류 응답을 반환값에 설정하고 `fail` 콜백을 호출합니다.

***

## db.getUserByToken 모듈

### Param:

* **userGroupId (string)**: 토큰을 검증할 유저 그룹 ID입니다.
* **token (string)**: 검증할 유저의 토큰입니다.

### Return:

* **result (object)**: 토큰 검증 후 얻은 유저 데이터입니다.

이 모듈은 제공된 토큰을 사용하여 특정 유저 그룹의 유저 정보를 조회합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보내고, 요청이 성공하면 유저 데이터를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 `fail` 콜백을 호출하며 오류 응답을 반환합니다.

***

## db.postCreate 모듈

### Param:

* **database (database)**: 데이터를 생성할 데이터베이스입니다.
* **query (queryObject)**: 생성할 데이터에 대한 쿼리 객체입니다.

### Return:

* **result (number)**: 데이터 생성 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에 새로운 데이터를 생성합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.postCreateBulkCSV 모듈

### Param:

* **database (database)**: 데이터를 추가할 데이터베이스입니다.
* **data (string)**: CSV 형식의 데이터 문자열입니다.

### Return:

* **result (number)**: 데이터 추가 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에 CSV 형식의 데이터를 대량으로 추가합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.\


***

## db.postCreateBulkJSON 모듈

### Param:

* **database (database)**: 데이터를 추가할 데이터베이스입니다.
* **data (string)**: JSON 형식의 데이터 문자열입니다.

### Return:

* **result (number)**: 데이터 추가 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에 JSON 형식의 데이터를 대량으로 추가합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.postCreateBulkXML 모듈

### Param:

* **database (database)**: 데이터를 추가할 데이터베이스입니다.
* **data (string)**: XML 형식의 데이터 문자열입니다.

### Return:

* **result (number)**: 데이터 추가 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에 XML 형식의 데이터를 대량으로 추가합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.postCreateMany 모듈

### Param:

* **database (database)**: 데이터를 추가할 데이터베이스입니다.
* **data (array of T)**: 데이터베이스에 추가할 데이터 목록입니다. 각 데이터 항목은 `T` 타입을 따릅니다.

### Return:

* **result (number)**: 데이터 추가 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에 여러 데이터 항목을 한 번에 추가합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.postCreateUser 모듈

### Param:

* **data (object)**: 추가할 유저 데이터입니다.
* **permit (permit)**: 유저 권한 설정 객체입니다. 이 객체는 유저 그룹 ID (`userGroupId`)와 권한 ID 리스트 (`permitIdList`)를 포함합니다.
* **email (string)**: 유저의 이메일 주소입니다.
* **password (string)**: 유저의 비밀번호입니다.

### Return:

* **result (number)**: 데이터 추가 작업의 결과 코드입니다. 성공적으로 유저를 추가하면 1, 실패 시 0을 반환합니다.

이 모듈은 새로운 유저 데이터를 지정된 데이터베이스에 추가합니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 유저 데이터가 데이터베이스에 추가되고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 응답 데이터를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.putUpdate 모듈

### Param:

* **database (database)**: 데이터를 수정할 데이터베이스입니다.
* **query (queryObject)**: 수정할 데이터의 조건을 명시하는 쿼리 객체입니다.
* **action (action of T)**: 데이터 수정 작업을 지정하는 액션 객체입니다. 이 객체는 수정 작업의 세부 내용을 포함하며, `pull`, `push`, `set` 등의 작업이 포함될 수 있습니다.

### Return:

* **result (number)**: 데이터 수정 작업의 결과 코드입니다. 성공 시 100, 실패 시 다른 코드를 반환합니다.

이 모듈은 지정된 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터를 수정합니다. 수정할 데이터와 작업의 내용은 `action` 객체를 통해 정의됩니다. `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보냅니다. 요청이 성공하면 성공 코드를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 코드를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.putUpdateManyTime 모듈

### Param:

* **database (database)**: 데이터를 수정할 데이터베이스입니다.
* **query (queryObject)**: 수정할 데이터의 조건을 명시하는 쿼리 객체입니다.
* **time (Array\<date>)**: 각 수정 작업을 실행할 예정 시간 목록입니다.
* **checkInId (Array\<string>)**: 각 수정 작업에 대한 고유 식별자 목록입니다.
* **value (Array\<string>)**: 수정 작업에서 사용될 값의 목록입니다.
* **action (action of T)**: 데이터 수정 작업을 지정하는 액션 객체입니다. 이 객체는 수정 작업의 세부 내용을 포함하며, `pull`, `push`, `set` 등의 작업이 포함될 수 있습니다.

### Return:

* 이 모듈은 직접적인 반환 값 없이 배치된 작업의 결과를 비동기적으로 처리합니다.

이 모듈은 주어진 시간에 맞춰 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터를 수정합니다. 수정은 `BullMQ`를 사용하여 예약된 작업으로 처리되며, `IORedis`를 통해 Redis 서버와 연결됩니다. 각 작업은 `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보내고, 예약된 시간에 실행됩니다. 작업이 성공하면 콘솔에 성공 메시지를 출력하고, 실패하면 에러 메시지를 출력합니다.

***

## db.putUpdateTime 모듈

### Param:

* **database (database)**: 데이터를 수정할 데이터베이스입니다.
* **query (queryObject)**: 수정할 데이터의 조건을 명시하는 쿼리 객체입니다.
* **time (date)**: 데이터 수정을 실행할 예정 시간입니다.
* **checkInId (string)**: 수정 작업에 대한 고유 식별자입니다.
* **action (action of T)**: 데이터 수정 작업을 지정하는 액션 객체입니다. 이 객체는 수정 작업의 세부 내용을 포함하며, `pull`, `push`, `set` 등의 작업이 포함될 수 있습니다.

### Return:

* 이 모듈은 직접적인 반환 값 없이 배치된 작업의 결과를 비동기적으로 처리합니다.

이 모듈은 주어진 시간에 맞춰 데이터베이스에서 `query` 객체에 정의된 조건에 맞는 데이터를 수정합니다. 수정은 `BullMQ`를 사용하여 예약된 작업으로 처리되며, `IORedis`를 통해 Redis 서버와 연결됩니다. 각 작업은 `axios` 라이브러리를 사용하여 서버에 HTTP POST 요청을 비동기적으로 보내고, 예약된 시간에 실행됩니다. 작업이 성공하면 콘솔에 성공 메시지를 출력하고, 실패하면 에러 메시지를 출력합니다.

***

## db.putUpdateUser 모듈

### Param:

* **data (object)**: 수정할 유저 데이터입니다.
* **permit (permit)**: 유저 권한 설정 객체입니다. 이 객체는 유저 그룹 ID (`userGroupId`)와 권한 ID 리스트 (`permitIdList`)를 포함합니다.
* **userId (string)**: 수정할 유저의 ID입니다.

### Return:

* **result (number)**: 데이터 수정 작업의 결과 코드입니다. 성공적으로 유저를 수정하면 1, 실패 시 0을 반환합니다.

이 모듈은 지정된 유저의 데이터를 수정합니다. `axios` 라이브러리를 사용하여 서버에 HTTP PATCH 요청을 비동기적으로 보냅니다. 요청이 성공하면 유저 데이터가 데이터베이스에서 수정되고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 응답 데이터를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.

***

## db.updateCustomValue 모듈

### Param:

* **userGroupId (string)**: 수정할 사용자가 속한 그룹 ID입니다.
* **userId (string)**: 수정할 사용자의 ID입니다.
* **keyValueObject (object)**: 수정할 사용자의 키-값 쌍 데이터입니다.

### Return:

* **result (object)**: 데이터 수정 작업의 결과 데이터입니다. 성공적으로 사용자의 커스텀 값을 수정하면 수정된 값의 데이터를 포함하는 객체, 실패 시 오류 메시지를 포함하는 객체를 반환합니다.

이 모듈은 지정된 유저의 커스텀 데이터 값을 수정합니다. `axios` 라이브러리를 사용하여 서버에 HTTP PATCH 요청을 비동기적으로 보냅니다. 요청이 성공하면 수정된 데이터를 반환하고 `success` 콜백을 호출합니다. 요청이 실패하면 실패 응답 데이터를 반환하고 `fail` 콜백을 호출합니다. 에러가 발생하면 에러 응답 데이터를 반환 값으로 설정하고 `fail` 콜백을 호출합니다.
