# string

## 개요

string은 문자에 대한 타입으로 데이터 형식은 문자를 나타내며 문자에 대한 제약사항을 지원합니다.

※ string은 다른 모든 문자 타입의 부모이며 Advanced Field의 모든 문자 타입들은 Primitive의 이 타입이 지원하는 기능 및 제약사항을 포함합니다.

## 제약사항

<table><thead><tr><th width="140">키워드</th><th width="154">제약 데이터 타입</th><th>작동 방식</th></tr></thead><tbody><tr><td>gte</td><td>number (0 &#x3C; )</td><td>입력한 숫자 이상의 텍스트 길이인지 검사</td></tr><tr><td>lte</td><td>number (0 &#x3C; )</td><td>입력한 숫자 이하의 텍스트 길이인지 검사</td></tr><tr><td>like</td><td>string</td><td>특정한 문자가 포함 되었는지 검사</td></tr><tr><td>in</td><td>string (array)</td><td>입력한 문자 리스트에 포함된 문자인지 검사</td></tr><tr><td>nin</td><td>string (array)</td><td>입력한 문자 리스트에 포함되지 않은 문자인지 검사</td></tr><tr><td>regex</td><td>string</td><td>입력된 정규식에 맞는 문자인지 검사</td></tr></tbody></table>
