### Orthonormal basis
- Orthonormal basis란 1 unit의 서로 각각 orthogonal한 basis vector들
- vector set B가 orthonromal basis라면 B에 포함된 vector들의 제곱은 1이고 서로 다른 vector들과의 곱은 0(두 벡터가 서로 orthogonal하면 곱이 0)이다
- Standard basis의 vector들을 alternate basis의 vector로 변환하려면 아래와 같은 matrix equation 사용 가능
![alt text](./images/Orthonormal%20basis%20and%20Gram-Schmidt-Orthonormal%20basis1.png)
- 만약 위 과정에서 orthonormal basis로 변환을 하는 경우 각 column vector들은 orthonormal set이 된다
- Orthogonal matrix는 columns들이 orthonormal set의 vector들로 이루어진 square matrix
- 만약 matrix가 rectangular지만 column들이 orthonormal set의 vector이면 orthonormal matrix
- Orthonormal basis를 활용하면 위 과정처럼 augemented matrix를 reduced-row-echelon form으로 만드는 것보다 아래처럼 orthonormal basis와 x의 dot product로 나타낼 수 있음
![alt text](./images/Orthonormal%20basis%20and%20Gram-Schmidt-Orthonormal%20basis2.png)

### Projection onto an orthonormal basis
- Subspace가 orthonormal basis로 구성된 경우 vector를 subspace로 projection하는 경우에도 더 간단히 수행 가능
- Vector x를 subspace V에 projection하는 것을 $$Proj_Vx=A(A^TA)^{-1}A^Tx$$로 표한할 수 있는데 subspace V가 orthonormal basis로 구성된 경우 $$Proj_vx=AA^Tx$$로 표현 가능
- A가 orthonormal column vector로 이루어진 경우 $$(A^TA)^{-1}$$를 identity matrix I로 단순화 가능하기 때문에 위가 성립

### Gram-Schmidt process for change of basis
- Gram-Schmidt process는 subspace의 basis를 orthonormal basis로 변환하는 process이다
- Gram-Schmidt process의 순서
  - subspace V가 $$v_1,v_2,v_3$$로 이루어져 있다고 가정한다
  - V=Span($$v_1,v_2,v_3$$)
  - 가장 먼저 $$v_1$$을 아래와 같이 normalize한다
  ![alt text](./images/Orthonormal%20basis%20and%20Gram-Schmidt-Gram-Schmidt%20process%20for%20change%20of%20basis%201.png)
  - 다음으로는 $$v_2$$를 $$u_1$$에 orthogonal하게 만드는 것으로 아래와 같은 식으로 수행할 수 있다
  ![alt text](./images/Orthonormal%20basis%20and%20Gram-Schmidt-Gram-Schmidt%20process%20for%20change%20of%20basis%202.png)
  - 위 식에 대해 설명하면 만약 $$v_2$$를 $$u_1$$으로 이루어진 span $$V_1$$에 projection하면 $$Proj_{v_1}v_2$$이 되고, $$w_2$$는 $$Proj_{v_1}v_2$$와 $$v_2$$를 연결하는 vector가 되므로 $$w_2=v_2-Proj_{v1}v_2$$이다
  - 또한 $$V_1$$은 $$u_1$$만을 가지기 때문에 basis의 모든 vector가 다른 vector에 orthogonal(vector가 1개뿐이므로)하고 $$u_1$$은 normal vecotr이므로 orthonormal subspace이다. 따라서 $$Proj_{v_1}v_2$$는 $$w_2=v_2-(v_2u_1)u_1$$으로 표현 가능하다
  - 그리고 이렇게 구한 $$w_2$$를 $$v_144과 같은 방식으로 normalize시키고 이것을 $$u_2$$로 정의한다
  - 이후로는 모든 vector에 대해 이전 vector들 모두에 orthogonal하고 normalize된 vector들을 구한다