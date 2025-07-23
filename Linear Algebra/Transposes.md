### Transposes and their determinants
- Transpose는 matrix의 row와 column을 바꾸는 연산
- 아래와 같이 row와 column의 순서가 변경
![alt text](./images/Transposes-Transposes%20and%20their%20determinants%201.png)
- 아래와 같이 row와 column이 달라도 transpose 연산 가능
![alt text](./images/Transposes-Transposes%20and%20their%20determinants%202.png)
- Square matrix는 transpose를 적용해도 determinant가 변하지 않음

### Transpose of products, sums, and inverses
- Transpose of product
  - Matrix product의 transpose는 각 matrix를 transpose하고 product 순서를 역순으로 한것과 동일
  - $$(XY)^T=Y^Tx^T$$
  - $$(XYZ)^T=Z^TY^TX^T$$
- Transpose of a matrix sum
  - Matrix sum의 transpose는 각 matrix의 transposed matrix의 sum
  - $$(X+Y)^T=X^T+Y^T$$
- Transpose of a matrix inverse
  - 어떤 matrix가 있을 때, 그 transpose matrix의 inverse matrix는 원래 matrix의 inverse matrix를 transpose한 것과 동일 
  - $$(X^T)^{-1}=(X^{-1})^T$$