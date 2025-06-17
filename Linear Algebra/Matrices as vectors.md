### Vector
- Vector는 두 가지 특성을 가짐
  - vector는 방향성을 가진다
  - vector의 단위는 vector의 길이를 나타냄
- Row vector와 column vector
  - Row vector는 하나의 row로 이루어진 vector이다.
  ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-vector-row%20vector.png)
  - Column vector는 하나의 column으로 이루어진 vector이다.
  ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-vector-column%20vector.png)
- Matrix에서 각 row는 row vector로, 각 column은 column vector로 볼 수 있다
- Vector는 방향과 길이만을 가지므로 시작점이 어디인지는 중요하지 않음
  - 시작점이 다르더라도 방향과 길이가 같으면 같은 vector

### Vector Operations
- Vector의 덧셈
  - Vector의 덧셈은 단순히 Vector의 구성요소들을 각각 더하는 연산이다
  - vector a가 (3,4)이고 b가 (-1,2)이라고 하면 아래와 같은 연산 결과를 얻을 수 있다
  ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-vector%20sum-예시.png) 
- Vector와 Scalar의 곱셈
  - Vector에 Scalar를 곱해주는 연산은 단수히 Vector의 구성요소들을 Scalar로 곱해주는 연산이다
  - vector a가 (3,4)일때 2를 곱해주면 아래와 같은 연산 결과를 얻을 수 있다
  ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-vector%20scalar%20mul-예시.png)
- Vector와 Vector의 곱셈
  - Vector와 Vector의 곱셈은 각 Vector의 구성요소들을 서로 곱해주는 연산이다
  ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-vector%20vector%20mul-예시.png)

### Unit Vector & Basis Vector
- Unit Vector
  - Unit Vector란 크기가 1인 Vector
  - 일반적으로 Unit vector는 특정한 방향성을 가지지 않아도 되며, 길이가 1이라면 Unit vector이다.
- Basis Vector
  - Basis Vector는 Unit Vector의 특별한 형태 중 하나
  - Basis Vector는 (1, 0)이나 (0, 1, 0)처럼 하나의 요소만 1이고 나머지는 모두 0인 Vector

### Span of vector set
- vector set의 span은 vector들의 linear combination을 통해 표현할 수 있는 vector들의 범위
- Linear Combination
  - Linear Combination은 vector들을 결합하는 것으로 vector i가 (1,0), vector j가 (0,1)이라고 하면 13i+2j로 (13,2)의 vector를 구하는 연산
  - 이런식으로 각각의 vector들을 결합해서 다양한 vector들을 만들 수 있다

### Span, and linear independence
- Linear Indepence는 vector set의 어느 한 vector가 다른 벡터들을 이용해 만들 수 있는 지 여부
- 2차원 공간에서는 Linear Indepence한 2개의 vector가 있으면 모든 2차원 vector 표현 가능
- 3차원 공간에서는 Linear Indepence한 3개의 vector가 있으면 모든 3차원 vector 표현 가능
- 차원의 크기와 Linear Indepence한 vector의 수가 같으면 해당 차원의 모든 vector 표현 가능
- 따라서 N차원에서는 N개 이상의 vector가 Linear Indepence 할 수 없다

### Linear Indepencence in $$R^2$$
- Linear dependence
  - vector가 서로 Linear dependence하다는 것은 특정 vector들의 조합을 통해 해당 vector를 만들 수 있다는 것
  - ![alt text](../Linear%20Algebra/images/Matrices%20as%20vectors-Linear%20Indepence%20in%20r2-two%20vectors.png)
  - 위 $$v_1⨉4=v_2$$이므로 두 vector는 서로 Linear dependence하다
- 만약 2차원 공간에서 3개 이상의 vector가 있으면 무조건 linear dependence하다