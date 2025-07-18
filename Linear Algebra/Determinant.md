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