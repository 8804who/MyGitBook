### Multpying matrices by vectors
- Vector와 Matrix의 곱은 Matrix 간의 곱과 동일
- Vector를 N ⨉ 1 dimension의 Matrix라고 생각하면 연산을 수행
- 만약 N ⨉ M Matrix와 M개의 원소를 가진 Vector를 곱하면 결과값의 dimension은 N ⨉ 1 

### Null Space
- Null Space란 m⨉n dimension의 행렬 A와 곱했을 때, 결과값이 무조건 zero-vector인 vecotr들로 이루어진 subspace
- 이를 A의 null space 혹은 N(A)로 표현
- null space는 subspace가 되기 위한 3가지 조건을 모두 충족하므로 항상 subspace이다

### Null space of a matrix
- Matrix A의 null space를 찾기 위해서는 A에 곱했을 때 zero-vector가 되는 vector set을 찾아야한다
- 예시
![alt text](../Linear%20Algebra/images/Matrix-vector%20products-Null%20space%20of%20a%20matrix%201.png)
- 위와 같은 Matrix A가 있을 때, A에 곱했을 때, zero-vector가 되는 vecotr를 [$$x_1, x_2, x_3$$]라고 한다
![alt text](../Linear%20Algebra/images/Matrix-vector%20products-Null%20space%20of%20a%20matrix%202.png)
- Matrix A의 null space N(A)를 찾기 위해서는 먼저 Matrix A를 reduced row-echelon form으로 만들어야 한다.
![alt text](../Linear%20Algebra/images/Matrix-vector%20products-Null%20space%20of%20a%20matrix%203.png)
- row-echelon form으로 변환을 완료하였다면 matrix의 equation들을 간단화시킨다.
![alt text](../Linear%20Algebra/images/Matrix-vector%20products-Null%20space%20of%20a%20matrix%204.png)
- 위 식에서 $$x_1 = 3x_3$$, $$x_2=-3x_3$$이므로 x1,x2,x3의 vector는 아래와 같이 나타낼 수 있다.  
![alt text](../Linear%20Algebra/images/Matrix-vector%20products-Null%20space%20of%20a%20matrix%205.png)
- 위와 같이 [3, -3, 1] vector는 A의 zero-vecotr이고 [3, -3, 1] vector의 linear combination들의 set이 null space가 된다

### Column space and Ax=b
- Column space
  - 어느 한 matrix의 Column space는 그 matrix의 column vector들로 만들 수 있는 모든 linear combination들로 정의할 수 있다
  - 만약 matrix A, vector x와 b가 Ax=b와 같은 관계이고, b가 A의 column들의 linear combination이면 이 식이 성립하는 vector x를 찾을 수 있다
- Linear independence and the null space
  - 만약 matrix A의 column vector들이 linear independent하면 그 column vector들이 column space의 basis를 형성한다고 할 수 있다
  - 반대로 matrix A의 column vector들이 linear dependent하면 그 column vector들은 basis를 형성할 수 없다.

### Solving Ax=b
- Complementary solution
  - Ax=0이라는 식에대한 Complementary solution은 Ax=0을 만족하는 vector set x를 뜻한다고 할 수 있다
- Particular solution
  - Ax=0대신 Ax=b라는 식이 있을 때, 이 식을 만족시키는 vecotr x을 Ax=b의 Particular solution이라고 할 수 있다
- General solution
  - Ax=b에 대한 General solution은 Ax=0과 Ax=b를 만족시키는 Complementary solution과 Particular solution의 합이다