### Orthogonal complements
- n차원 공간 상의 vector set V의 orthogonal complement를 $$V^⫠$$(V_perp)라 하고, $$V^⫠$$의 모든 vector는 V의 모든 vector와 orthogonal하다
- 만약 vector v의 set V와 vector x의 set $$V^⫠$$가 있으면 v의 모든 vector는 x의 모든 vector와 orthogonal하고 따라서 두 vector set의 dot product는 0이 된다
- $$V^⫠$$ is a subspace
  - $$V^⫠$$도 subspace로 addition과 multiplication에 닫혀있다
  - $$V^⫠$$의 vector x1과 x2의 addition도 V의 모든 vector와 orthogonal하다
  - $$V^⫠$$의 vector x1에 scalar c를 multiply해도 V의 모든 vector와 orthogonal하다
- Complement of the complement
  - Orthogonal complement의 orthogonal complement는 original subspace와 동일
  - $$(V^⫠)^⫠=V$$
  - 만약 $$V^⫠$$와 $$(V^⫠)^⫠=V$$의 모든 vector가 orthogonal하고, $$V^⫠$$와 V의 모든 vector가 orthogonal하기 때문에 $$(V^⫠)^⫠=V$$가 성립

### Orthogonal complements of the fundamental subspaces
- null space N(A)와 row space C($$A^T$$)는 $$N(A)=(C(A^T))^⫠$$이므로 orthogonal complement이다
- left null space $$N(A^T)$$와 column space C(A)는 $$N(A^T)=(C(A))^⫠$$이므로 orthogonal complement이다
- row space와 null space는 서로 orthogonal하고 column space와 left null space는 서로 orthogonal하다
- 따라서 row space와 null space, column space와 left null space는 각각 zero vector에서만 교차한다
- Dimension of the orthogonal complement
  - subspace V와 $$V^⫠$$의 dimension의 합은 항상 두 subspace가 속해있는 space $$R^n$$의 dimesnsion과 동일하다
  - Dim(V)+Dim($$V^⫠$$)=n

### Projection onto the subspace
- Line L위에 vector x를 projection한 vector를 $$Proj_Lx$$, L위의 한 점에서 x의 마지막 부분이 연결되었고 L과 orthogonal한 vector를 $$x-Proj_Lx$$라 할 수 있다
- $$Proj_Lx$$를 v로, $$x-Proj_Lx$$를 w에 대입하면 x-v=w이고 이는 x=v+w로 쓸 수 있다
- w가 L에 orthogonal하기 때문에 v는 L에 포함된 vector이고 w는 $$L^⫠$$에 포함된 vector이다
- Vector를 line에 projection하는 것처럼 subspace에도 projection 할 수 있음
- 만약 subspace V에 projection된 vector $$Proj_vx$$가 있으면 vector x는 V의 모든 vector들 중 $$Proj_vx$$와 가장 가깝다
- Projection is a linear transformation
  - subspace V에 vector x를 projection하는 것은 linear transformation으로 볼 수 있다. 
  -subpsace와 vectordml projection을 matrix-vector product로 보면 $$Proj_vx=A(A^TA)^{-1}A^Tx$$로 쓸 수 있고 여기서 A는 subspace V의 column vector를 이루는 basis들의 matrix이다
  - 참고로 위 식은 A가 square이고 invertible하지 않은 이상 $$Proj_vx=A(A)^{-1}(A^T)^{-1}A^Tx$$ 형식으로 풀어쓸 수 없다
  - 만약 A가 invertible하면 A는 $$R^n$$ 전체를 정의하게 되므로, vector x를 V에 projection하면 값은 그대로 x가 됨
  - 만약 A가 invertible(square는 invertible의 필수 요건이므로 생략)하지 않으면 $$(A)^{-1}$$와 $$(A^T)^{-1}$$를 구할 수 없으므로 square matrix $$(A^TA)$$의 inverse matrix를 구한다
  
  ### Least squares solution
  - Ax=b에서 b가 A의 column space에 존재하지 않으면 A의 linear combination으로 b를 만들 수 없다는 뜻이 되고 이 경우 Ax=b의 해는 존재하지 않는다
  - 만약 해가 존재하지 않는 경우 해에 가장 가까운 값을 찾는 것을 목적으로 하는데 least square solution은 해에 가장 가까운 값을 찾는 방법 중 하나이다
  - b에 가장 가까운 Ax의 least square solution을 $$Ax^*$$라고 한다
  - $$Ax^*$$는 b에 가장 가까운 값이므로 $$A^TAx^*=A^Tb$$를 만족할 것이다
  - 따라서 $$A^TA$$와 $$A^Tb$$를 구한 후 그를 통해 $$x^*$$를 구할 수 있다