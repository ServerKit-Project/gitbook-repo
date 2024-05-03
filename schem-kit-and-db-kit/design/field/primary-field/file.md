# file

## 개요

file은 파일에 대한 타입으로 데이터 형식은 객체를 나타냅니다.

파일로 지정된 필드는 실제 업로드한 파일 정보를 매칭하며 mimetype(확장자), size(파일 용량), filename(파일 실제 이름)을 나타냅니다.

mimetype은 MDN에서 표출하는 Media Type을 사용하며 아래 사이트를 참고해주세요.

[https://www.iana.org/assignments/media-types/media-types.xhtml](https://www.iana.org/assignments/media-types/media-types.xhtml)

※ file은 다른 모든 파일 타입의 부모이며 Advanced Field의 모든 파일 타입들은 Primitive의 이 타입이 지원하는 기능 및 제약사항을 포함합니다.

## 제약사항

<table><thead><tr><th width="140">키워드</th><th width="154">제약 데이터 타입</th><th>작동 방식</th></tr></thead><tbody><tr><td>gte</td><td>number (0 &#x3C; )</td><td>입력한 숫자 이상의 파일 용량인지 검사</td></tr><tr><td>lte</td><td>number (0 &#x3C; )</td><td>입력한 숫자 이하의 파일 용량인지 검사</td></tr><tr><td>in</td><td>string (array)</td><td>입력한 문자 리스트에 포함되는 확장자인지 검사</td></tr><tr><td>nin</td><td>string (array)</td><td>입력한 문자 리스트에 포함되지 않는 확장자인지 검사</td></tr></tbody></table>
