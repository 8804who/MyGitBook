### Eigenvalues, eigenvectors, eigenspaces
- Transformation T의 eigenvector는 T(v)=λv를 만족하는 vector v
- 위에서 λ는 eigenvalue로 eigenvector v와 연관이 있다
- T(v)=λv의 식을 해석해보면 T(v)가 그저 scale이 λ가 된 vector v라는 뜻
- v와 T(v)는 길이는 다르지만 결국 같은 선위에 존재하고, 따라서 T(v)가 v와 같은 span을 갖는 경우 v는 eigenvector라고 할 수 있음
- Finding eigenvalues
  - T(v)는 linear transformation Av와 같다고도 볼 수 있고 T(v)=Av=λv로 λ는 A와 같다고 볼 수 있다
  - 만약 A가 2⨉2라면 eigenvector는 2개가 존재하고 3⨉3이라면 eigenvecotr는 3개가 존재
  - v=O인 경우 eigenvalue λ를 정의할 수 없으므로, 이 경우 Av=λv가 성립해도 eigenvector로 포함하지 않는다
  - eignenvalue는 $$|λI_n-A|=O$$에서 얻은 system의 해이다
  - 참고로 Matrix A의 Trace(A)는 eigenvalue들의 합이고 Det(A)는 eigenvalue들의 곱이다
- Finding eigenvectors
  - Eigenvector를 찾기 위해서는 각 eigenvalue들의 eigenspace를 정의해야한다
  - Eigenvalue λ의 eigenspace $$E_λ$$는 Av=λv를 만족하는 모든 eigenvector v들의 set이다
  - Av=λv를 $$(λI_n-A)v=O$$로 표현 가능하고 $$λI_n-A$$는 matrix이므로 eigenspace는 matrix $$λI_n-A$$의 nullspace이고 $$E_λ=N(λI_n-A)$$

### Eigen in three dimensions
- 3⨉3 matrix에서도 eigenvalue를 찾는 과정은 동일
- 3차원에 대한 고려를 해야하는 것은 좀 더 복잡하지만 기본적으로 2⨉2일때와 동일