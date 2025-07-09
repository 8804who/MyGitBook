### Functions and transformations
- Function vs Transformation
  - Transformation은 실수의 Function과 유사하다고 볼 수 있다
  - Transformation은 vector를 또 다른 vector로 mapping하는 것
- Domain, codomain, range
  - Domain(정의역)은 mapping을 하려는 vector들의 set
  - Codomain(공역)은 mapping이 되는 vector들의 set
  - Range(치역)는 Codomain에서 실제로 mapping이 된 vector들의 set

### Transformation matrix and the image of the subset
- Transformation matrix
  - Transformation matrix는 transfomration의 vector나 vector set의 위치를 변환시키는 transformation의 series로 볼 수 있다
  - 만약 2⨉2 transformation matrix가 있다면 첫 번째 column은 vector i(1,0)과 vector j(0,1)에게는 서로 다른 transformation을 적용시킨다
- Image and preimage
  - 어떤 transformation이 적용되기 전의 vector를 preimage라고 한다
  - 그리고 transformation이 적용된 후의 vector를 image라고 한다

### Preimage, image, kernel
- Transformation as subspaces
  - Transformation은 언제나 addition과 multiplication에 닫혀있다
  - 따라서 Transformation은 언제나 subspace이다
  - 예를 들어 Q라는 space에 T라는 transformation을 적용하면 T(Q)는 subspace라고 할 수 있다
- Finding the preimage from the image
  - 만약 A의 subset a에 transformation을 적용한 결과가 B의 subset b라고하면 T(a)를 a의 image라고 한다
  - 만약 반대로 A에서 b로 mapping되는 모든 point의 set을 b의 preimage라고 한다
- Kernel
  - Transformation 결과가 zero vector인 모든 vector들의 set을 kernel이라하고 Ker(T)라고 표기한다

### Linear transformations as matrix-vector products
- Linear transformation은 matrix와 vector의 product로도 볼 수 있다
- 예를 들어 2차원의 vector(2⨉1)를 3차원의 vector(3⨉1)로 transform한다고하면 해당 vector에 transformation matrix(3⨉2)를 multiply하여 (3⨉2)⨉(2⨉1)의 결과로 (3⨉1)의 결과를 얻을 수 있다

### Linear transformation as rotation
- Rotation matrix를 통해 vetor를 회전시키는 연산도 가능
- 2차원 vector를 θ도만큼 회전 시키는 matrix는 아래와 같다
![alt text](./images/Transformations-Linear%20transformation%20as%20rotation%201.png)
- 3차원에서는 회전을 할 때 한 축을 기준으로 회전하고, 각 축을 기준으로 3차원 vector를 θ도만큼 회전 시키는 matrix는 아래와 같다. 
![alt text](./images/Transformations-Linear%20transformation%20as%20rotation%202.png)
- $$Rot_θ(u+v) = Rot_θ(u)+Rot_θ(v)$$가 성립
- $$Rot_θ(c⨉u) = c⨉Rot_θ(u)$$가 성립 

### Adding and scaling linear transformations
- Sums of transformations
  - 만약 n차원에서 m차원으로 변환하는 두 개의 transformation S와 T가 있을 경우, S(v)+T(v)=(S+T)(v)와 같다
  - 두 matrix의 addtion 결과로 나온 matrix를 transformation matrix로 사용한 transformation U(v) = S(v)+T(v)이다
- Scaled transformations
  - Transformation을 scalar를 통해 multiply하는 연산도 가능
  - T(x)를 scalar c로 multiply하면 cT(x)가 된다
  - T()의 transformation matrix를 scalar로 multiply하면 새로운 transformation matrix를 얻을 수 있다 