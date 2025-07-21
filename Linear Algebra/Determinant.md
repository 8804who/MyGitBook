### Determinant
- Determinant for 2⨉2 matrix
  - 2⨉2 matrix의 determinant는 아래와 같이 matrix가 있을 때, $$ad-bc$$로 구할 수 있다.
  ![alt text](./images/Determinant-Determinant%201.png)
- Determinant for 3⨉3 and n⨉n matrices
  - 3⨉3 matrix의 determinant는 아래와 같이 구할 수 있다.
  ![alt text](./images/Determinant-Determinant%202.png)
  - 3⨉3 matrix의 determinant를 구하는 과정은 아래와 같다.
    1. 한 row나 column을 선택
    2. 해당 row 또는 column의 entry들을 하나씩 순차적으로 연산을 수행한다
    3. 해당 entry가 포함된 row와 column을 제외하고 남은 4개의 entry들을 2⨉2 matrix로 취급하고 해당 matrix의 determiant를 구한다
    4. 3에서 구한 determinant와 2에서 선택한 entry를 곱한다.
    5. 4에서 구한 determinant와 entry의 곱을 모두 합한다
    6. 이때 entry가 홀수 row의 홀수 column이면 +, 홀수 row의 짝수 column이면 -, 짝수 row의 홀수 column이면 -, 짝수 row의 짝수 column이면 + 부호를 붙인다.
    7. 6에 따라 구한 총합이 해당 matrix의 determiant이다
  - n⨉n matrix의 determinant를 구하는 과정은 3⨉3 matrix와 동일
    - 한 row나 column을 선택
    - 선택된 구역의 entry들과 그 entry가 포함된 row와 column을 제외하고 남은 entry들로 만들어진 n-1⨉n-1 matrix의 determinant를 구하여 연산을 수행
- Rule of Sarrus
  - 3⨉3 matrix의 determinant를 구하는 방식 중 하나
  ![alt text](./images/Determinant-Determinant%203.png)
  - 위와 같은 matrix A가 있을 경우 아래와 같이 확장
  ![alt text](./images/Determinant-Determinant%204.png)
  - Matrix의 대각선 entry들을 서로 묶어줌 
  ![alt text](./images/Determinant-Determinant%205.png)
  - 위에서 묶은 entry들을 서로 곱하고 왼쪽 위에서 오른쪽 아래로 향하는 대각선은 +, 왼쪽 아래에서 오른쪽 위로 올라가는 대각선은 - 계수를 적용하여 모두 합하여주면 그 값이 determinant
  - 식으로 나타내면 $$aei+bgf+cdh-afh-bdi-ceg$$로 나타낼 수 있음

### Cramer's rule for solving systems
- Cramer's rule은 determinant를 이용해 linear system을 푸는 방식
- 각 variable의 해는 $${D_v}\over{D}$$로 구할 수 있음
- 여기서 $$D_v$$는 해를 구하려는 variable column에 answer column을 대입한 coefficient matrix의 determinant이고 D는 coefficient matrrix의 determinant
- 예를 들어 아래와 같은 식의 $$D$$와 $$D_v$$ 예시는 다음과 같다.
![alt text](./images/Determinant-Cramer's%20rule%20for%20solving%20systems%201.png)
![alt text](./images/Determinant-Cramer's%20rule%20for%20solving%20systems%202.png)

### Modifying determinants
- Multiplying a row or a column by a scalar
  - 2⨉2 Matrix A의 determinant가 |A|일 때, A의 한 row나 column에 scalar k를 곱하여 만든 Matrix B의 determinant |B|는 k|A|와 같다
  - A의 모든 row 또는 column에 scalar k를 곱하여만 든 Matrix B의 determinant |B|는 $$k^2|A|$$와 같다
- Sum of two rows
  - 만약 3개의 identical matrix A, B, C가 존재하고 각 matrix의 한 가지 row만 값이 다르고, 두 matrix의 해당 row를 합한 것이 나머지 한 matrix의 해당 row와 같을 경우, 두 matrix의 determinant의 합은 나머지 한 matrix의 derterminant와 같다
- Swapped and duplicate rows
  - 만약 Matrix A에서 특정 두 행의 순서를 바꾼 Matrix B의 determinant는 -|A|와 같다
  - 그런데 만약 순서를 바꾼 두 행이 서로 같은 identical row일 경우 determinant는 변하지 않는다
- Row operations don't change the determinant
  - Row에 특정 scalar를 곱하는 연산 외에 다른 Row operation들은 marix의 determinant를 바꾸지 않는다

### Upper and lower traingular matrices
- Upper traingular matrix & Lower traingular matrix
  - Upper triagular matrix는 대각선 아래의 모든 entry들이 0인 matrix
  ![alt text](./images/Determinant-Upper%20and%20lower%20traingular%20matrices%201.png)
  - Lowser triangular matrix는 대각선 위의 모든 entry들이 0인 matrix
  ![alt text](./images/Determinant-Upper%20and%20lower%20traingular%20matrices%202.png)
- Determinant of triangular matrices
  - Upper traingular matrix나 Lower triangular matrix도 determinant 계산 가능
  - Triangular matrix의 determinant는 대각선 entry들의 곱
  - Matrix를 Triangular matrix로 변환 후 determinant를 구하는 방법도 사용 가능