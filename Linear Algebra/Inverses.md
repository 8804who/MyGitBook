### Inverse of a transformation
- Identity transformation
  - Identity transformation은 주어진 vector 그대로를 mapping하는 transformation이다
  - 예를 들자면 vecotr v가 있을 때, T(v) = v인 transformation을 identity transformation이라고 한다
- Invertibility and inverse transformation
  - 만약 vector a에 transformation을 적용해 vector b로 만들고, 그 vector b에 transformation을 적용해 다시 vector a로 만들 수 있다면 invertanle하다고 한다
  - 다른 말로하면, invertible하다는 것은 inverse를 가진다는 것이다
  - A -> B로 변환하는 transformation T의 inverse는 $$T^{-1}$$로 표현하고 B -> A로 변환하는 transformation이다
- Invertibility and uniqueness
  - Transformation이 invertible하면 inverse transformation은 unique하다. 따라서 하나의 transformation은 여러개의 inverse를 가질 수 없다
  - Invertible ransformation의 결과값은 언제나 같다. T(a)의 결과가 b라면 항상 b만 얻을 수 있다. 이외의 결과값은 나올 수 없다
  - Inverse transformation의 결과괎은 언제나 같다. $$T^{-1}(b)의 결과가 a라면 항상 a만 얻을 수 있다. 이외의 결과값은 나올 수 없다
- Surjective and injective
  - Invertible transformation과 inverse transformation은 항상 surjective하고 injective하다
  - 입력값과 결과값은 항상 1대1로 대응하고 하나의 입력값에서 서로 다른 결과값이 나오거나, 서로 다른 입력값에서 하나의 결과값이 나올 수 없다

### Invertibility from the matrix-vector product
- 만약 column space m이 codomoin $$R^m$$ 전체일 경우 transformation T는 surjective하다
  - Columns space M이 codomain $$R^m$$ 전체인 경우는, M의 reduced row-echelon form이 m개의 pivot entry를 가지고 각 행에 하나의 pivot entry를 가질때이다
  - 다르게 말하면 m개의 basis vector가 columns space M을 구성한다는 것이다
- Square matrix만 invertible하다
  - Transformation이 surjective하려면 M의 rank가 m이어야한다. 이 말은 모든 row에 pivot entry가 있어야한다는 뜻이다
  - Transformation이 injective하려면 M의 rank가 n이어야한다. 이 말은 모든 column에 pivot entry가 있어야한다는 뜻이다
  - Rank(M)=m=n이라는 말은 row와 column의 크기가 같다는 말이다.
  - 따라서 Square matrix만이 surjective하면서 injective할 수 있으므로 square matrix만이 invertible할 수 있다
  - 단, square matrix라고 반드시 invertible하지는 않다

### Inverse transformations are linear
- Inverse transformation 역시도 linear transformation
- 따라서 inver transformation $$T^{-1}$$은 addition과 multiplication에 닫혀있다
- Inverse transformation도 linear transformation이므로 matrix-vector product로 표현 가능, $$T^{-1}(x)=A^{-1}x$$
- Inverse transformation의 matrix를 찾는 것은 일반 matrix의 inverse matrix를 구하는 방법과 동일

### Matrix inverses, and invertible and sibgular matrices
- Matrix inverse는 matrix의 division으로도 생각할 수 있다.
- 실수 $$R$$과 $$R$$의 역수 $$R^{-1}$$의 곱이 1인것처럼 matrix도 $$M$$과 $$M^{-1}$$이 idnetity matrix I가 된다고 생각할 수 있다
- Inverse matrix를 찾는 방법은 Matrix를 Idnentity Matrix로 augment한 후 reduced row-echelon form을 구하는 방식이 있다
- 이외에도 determinant을 이용하여 inverse matrix를 구하는 방법도 있다
![alt text](./images/Inverses-Matrix%20inverses,%20and%20invertible%20and%20sibgular%20matrices.png)
- 위는 matrix M의 determinant |M|을 이용해 inverse matrix를 구하는 방법이다
- 위 방식에서 오른쪽 matrix의 각 요소를 |M|으로 나누어 inverse matrix를 구한다. 그런데 만약 |M|이 0이라면 계산이 불가능할 것이다. 따라서 |M|이 0인 경우 그 matrix는 invertible하지 않다
- 만약 matrix가 invertible하지 않은 경우, 해당 matrix를 singular matrix라고 한다

### Solving systems with inverse matrix
- Inverse matrix를 이용해 system을 푸는 방법도 있음
- Linear system은 coefficient matrix와 변수 column vecotr(x,y)의 곱과 결과값 column vector(f, g)으로 표현 가능
- Linear system을 Coefficient matrix M과 변수 column vecotr a의 곱, 결과값 column vector b로 나타내면 $$Ma=b$$로 표현 가능
- 만약 양변에 inverse matrix $$M^{-1}$$을 곱하면 $$M^{-1}Ma=a=M^{-1}b$$의 식을 얻을 수 있음
- 따라서 $$M^{-1}b$$의 결과값이 각 변수의 해