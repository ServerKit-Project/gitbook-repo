# Advanced Field

## 개요

Advanced Field는 Primary Field를 바탕으로 더욱 고차원으로 추상화된 필드로 어떤 특수 목적을 위해 사용하고자 할 때 유용하게 사용할 수 있습니다.

예를 들어 문자(string)지만 email 형식의 문자를 사용하고자 한다면 Advanced Field에서 제공하는 string.email 필드를 사용할 수 있습니다.

사용자는 이러한 Advanced Field에서 제공하는 다양한 고추상화 필드로 더욱 효과적인 데이터 구조를 설계하고 제공할 수 있습니다.

## 네이밍 규칙

Advanced Field는 필드명에 일종의 규칙이 있습니다.

Advanced Field는 Primitive를 기반으로 만들어진 고추상화 필드로 Advanced는 반드시 어떠한 Primitive 필드의 모든 특징과 기능을 가지고 있습니다. **일종의 상속관계**로 Advanced 필드가 다른 Advanced 필드를 상속할 수도 있습니다.

이를 표현하기 위해 네이밍을 다음과 같이 지정합니다.

<figure><img src="../../../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Primitive, Advanced Field간 네이밍</p></figcaption></figure>

앞은 해당 Advanced Field가 상속한 필드명이 들어가고 뒤는 Advanced의 이름이 표출됩니다. 필드별 구분은 point(.) 으로 됩니다.
