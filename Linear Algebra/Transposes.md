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

### Null and column spacs of the transpose
- Transpose는 matrix의 row와 column을 바꾸는 연산이므로 $$A^T$$의 columns space는 $$A^T$$의 column이면서 동시에 $$A$$의 row
- 따라서 $$A^T$$의 column space를 A의 row space라고도 함
- Row space도 column space처럼 A의 row들의 linear combination
- $$A^T$$의 null space는 $$x^TA=O^T$$를 만족하는 vector set $$x^T$$이다
- $$x^TA=O^T$$로 $$x^T$$가 product 연산의 왼쪽에 있으므로 left null space라고도 함
- $$A^T$$의 column space의 dimension은 항상 A의 rank와 동일
- $$A^T$$의 null space를 구성하기위해 필요한 vector의 개수는 A의 row 수와 rank에 따라 달라짐