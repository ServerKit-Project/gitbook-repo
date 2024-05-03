# Attribute

## 개요

속성은 데이터 구조를 이루는 컬럼(Column)의 속성 값을 나타내는 값으로 데이터의 성질을 정의합니다.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### **NULL 허용 (canBeNull)**

데이터의 필드 타입과 상관 없이 NULL 데이터가 들어갈 수 있는 이중 타입을 허용한다. 예를 들어 필드 타입이 `string`인 상태로 canBeNull이 true가 되는 경우 `string | null` 타입으로 변경됩니다.

### 배열  (isArray)

체크 시 데이터 필드타입에 따라 해당 데이터가 배열 형식으로 변경됩니다. 예를 들어 필드 타입이 `string`일 경우 `string[]` 타입으로 변경됩니다.
