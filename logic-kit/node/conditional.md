# Conditional

#### IsNull 노드 (IsNull Node)

**목적:** 주어진 값이 `null`인지 아닌지 확인합니다.

**기능:** 이 노드는 입력된 값이 `null`인 경우 `true` 출력을 활성화하고, 그렇지 않으면 `false` 출력을 활성화합니다. 이를 통해 데이터의 존재 여부를 확인할 수 있으며, 로직의 흐름을 결정하는 데 사용됩니다.

#### Nullish Coalescing 노드 (Nullish Coalescing Node)

**목적:** 목표 변수가 `null`이나 `undefined`일 경우 기본 값을 제공합니다.

**기능:** `??` 연산자는 왼쪽 피연산자(`Target`)가 `null` 또는 `undefined`인 경우 오른쪽 피연산자(`Default`)를 반환합니다. 이는 기본 값을 설정하거나 변수가 비어 있을 때 안전하게 처리를 계속하려는 경우에 유용합니다.

#### HasValue 노드 (HasValue Node)

**목적:** 주어진 값에 유효한 데이터가 존재하는지 확인합니다.

**기능:** 이 노드는 입력된 값에 데이터가 존재하면 `true`를, 값이 `null`이나 `undefined`이면 `false`를 출력합니다. 값의 유효성을 판단하고 이를 바탕으로 로직의 흐름을 제어하는 데 사용됩니다.

####
