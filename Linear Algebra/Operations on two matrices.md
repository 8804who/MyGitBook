### Matrix addition & subtraction
- Matrix의 덧셈과 뺄셈은 두 Matrix의 dimension이 같은 경우에만 수행 가능
- 두 Matrix에서 같은 위치에 있는 Entry들 간에 덧셈이나 뺄셈을 수행
![alt text](../Linear Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Matrix%20addition%20&%20subtraction-연산%20예시.png)
- 예시로 2⨉2 Matrix들 간의 덧셈 연산은 위와 같이 수행

### Scalar multiplication
- Matrix에 Scalar를 곱해주는 연산도 수행 가능
- Matrix의 각 Entry에 Scalar를 곱해주는 방식으로 연산 수행
![alt text](../Linear Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Scalar%20multipication-연산%20예시.png)

### Zero Matrix
- Zero Matrix는 모든 entry가 0으로 이루어진 matrix
- 서로 더했을 때 결과값이 Zero Matrix가 되는 Matrix K와 -K를 opposite matrix라고 한다.

### Matrix multiplication
- Matrix간의 곱은 Scalar multiplication과 다르게 각 행과 열의 entry 들의 곱한 후 그 합을 구하는 연산을 수행
- Matrix multiplication A·B는 Matrix A의 column 수와 Matrix B의 row 수가 같아야만 수행 가능
- Matrix multiplication A·B를 수행하면 결과값은 A의 row 수 ⨉ B의 column 수 dimension
- Matrix multiplication 연산에는 보통 dot product 연산을 이용<br>
![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Matrix%20multipication-연산%20예시%201.png)
 - 만약 2⨉2 Matrix 간의 dot product를 수행하면 위와 같이 값을 구할 수 있다.
- dot product 연산 예시
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Matrix%20multipication-연산%20예시%202.png)
  ![alt text](..Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Matrix%20multipication-연산%20예시%203.png)
- A·B != B·A
- (AB)C = A(BC)
- A(B+C) = AB+AC

### Identity Matrix
- Identity Matrix는 어떤 Matrix에 곱했을 때 그 Matrix의 값이 그대로 나오는 Matrix
- Identity Matrix는 반드시 square matrix여야하고 대각선의 entry들이 1, 나머지 entry들은 모두 0으로 이루어져 있다.
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Identity%20Matrix%20예시.png)
- Identity Matrix와 다른 Matrix A를 곱하면 아래와 같이 Matrix A가 그대로 나온다.
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20two%20matrices-Identity%20Matrix%20연산%20예시.png)

### Elimination Matrix
- Elimination Matrix는 Matrix A에 곱했을 때 결과값이 Identity Matrix가 되는 Matrix
- 이후에 Inverse Matrix라는 이름으로 다시 배울 예정