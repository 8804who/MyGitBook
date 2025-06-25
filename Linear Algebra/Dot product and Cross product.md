### Dot product
- Dot product는 두 Vector가 얼마나 같은 방향을 향하는지 표시
- Dot product는 두 Vector에서 같은 순서의 요소들을 곱한 후 그 값들을 모두 합하여 구한다
![alt text](../Linear%20Algebra/images/Dot%20product%20and%20Cross%20product-Dot%20product%20예시.png)
- Dot product는 교환 법칙, 분배 법칙, 결합 법칙이 성립

### Cauchy-Schwarz inequality
- Cauchy-Schwarz inequality를 이용해 Vector가 linear dependent한지 확인 가능
- 두 Vector의 내적의 절대값과 두 Vector의 길이의 곱이 같을 경우 두 Vector는 linear dependent
- Cauchy-Schwarz inequality의 수식은 아래와 같음
![alt text](../Linear%20Algebra/images/Dot%20product%20and%20Cross%20product-Cauchy-Schwarz%20inequality.png)

### Vector traingle inequality
- Traingle inequality는 삼각형에서 짧은 두 변의 길이의 합은 나머지 한 변의 길이보다 크거나 같다는 의미의 $$c<=a+b$$
- 아래와 같이 삼각형의 각 점을 잇는 변을 vector라고 할 때 $$||u+v||<=||u||+||v||$$
![alt text](../Linear%20Algebra/images/Dot%20product%20and%20Cross%20product-Vector%20triangle%20inequality.png)
- 만약 $$||u+v||=||u||+||v||$$일 경우 아래 그림과 같이 vector $$u와$$ $$v$$는 동일선상에 존재하므로 linear dependent한 상태
![alt text](../Linear%20Algebra/images/Dot%20product%20and%20Cross%20product-Vector%20triangle%20inequality2.png)
- Vector triangle inequality는 dimension에 상관 없이 사용 가능

### Angle between vectors
- 두 vector의 내적은 두 vector 각각의 길이와 두 vector 사이의 각도의 코사인 값을 곱한 값
![alt text](../Linear%20Algebra/images/Dot%20product%20and%20Cross%20product-Angle%20between%20vectors.png)
- 두 vector가 서로 수직(perpendicular)인 경우 $$cos(90º) = 0$$이므로 두 vector의 내적은 0
- 두 vector가 수직인 경우 두 vecotr가 직교(orthogonal)한다고 한다.

### Equation of a plane, and normal vectors
- Plane은 3차원 공간에서의 평평한 도형
- Plane은 어느 한 normal vector와 perpendicular한 모든 vector들의 set
- plane의 equation은 $$Ax+By+Cz=D$$ 형식이고 normal vector n이 $$(A, B, C)$$라고 하면 plane의 equation은 $$a(x-x_0)+b(y-y_0)+c(z-z_0)=0$$이라고 할 수 있다
- 두 vector가 perpendicular할 경우 dot proudct 값은 0이 되므로 어느 한 normal vector와의 내적값이 0인 vector들의 set은 plane이라고 할 수 있다
- 만약 어느 한 plane이 $$Ax+By+Cz=D$$일 경우, 해당 plane의 normal vector n은 $$(A, B, C)$$이다
- 위가 성립하는 이유는 $$D$$가 어느 한 plane에 대해서 불변이기 때문이다. 어떤 plane에 대해 $$D$$는 shift할 수 있지만, 그래도 normal vector는 변하지 않는다.
- $$Ax+By+Cz=0$$, $$Ax+By+Cz=-7$$, $$Ax+By+Cz=e$$ 모두 같은 normal vector를 가지고 plane의 위치가 shift하는 것이다 
