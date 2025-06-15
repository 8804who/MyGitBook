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