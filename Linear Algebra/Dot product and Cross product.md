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
