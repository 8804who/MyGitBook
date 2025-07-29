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