# Variable

#### 변수와 Getter/Setter

서버키트의 로직키트에는 로직의 상태 또는 데이터를 저장하고 관리할 수 있는 '변수' 기능이 포함되어 있습니다. 이 변수들을 관리하기 위해 주로 사용되는 두 가지 유형의 노드는 'Getter'와 'Setter'입니다.

**Getter**

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**개요**: Getter는 설정된 변수에서 값을 읽어오는 역할을 합니다. **기능**: 이 노드는 output flowpin만을 가지고 있으며, 연결된 변수에서 데이터를 가져와 다음 노드로 전달합니다. Getter는 복잡한 로직 내에서 데이터를 추출할 때 사용되어, 로직의 다른 부분에서 이 값을 활용할 수 있도록 합니다.

**Setter**

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**개요**: Setter는 변수에 값을 설정하는 역할을 합니다.&#x20;

**기능**:

* **Input Parameter Pin**: Setter 노드는 입력 파라미터 핀을 통해 새로운 값을 받습니다. 이 값은 변수에 저장될 데이터입니다.
* **Input Flowpin**: 로직의 흐름에서 이 노드로 데이터가 어떻게 도달하는지를 결정합니다. 이 핀을 통해 Setter 노드가 활성화됩니다.
* **Output Flowpin**: 데이터 설정 후, 로직의 다음 단계로 흐름을 계속 이어갈 수 있도록 합니다. 이 핀은 Setter 노드의 작업 완료 후 다음 노드로의 연결을 가능하게 합니다.

**활용 예**: 사용자는 Setter를 통해 특정 변수에 사용자 입력값이나 계산 결과를 저장할 수 있으며, Getter를 사용하여 이 값을 다른 부분의 로직에서 재사용할 수 있습니다. 이는 데이터의 일관성을 유지하고, 중복 계산을 피하는 데 유용합니다.
