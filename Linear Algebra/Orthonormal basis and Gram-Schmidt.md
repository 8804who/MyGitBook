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