### 변수와 방정식이 2개인 Linear System
- 대입법
  - 순서
    1. 하나의 방정식을 한 변수에 대해 풀이합니다.
    2. 1단계에서 얻은 식을 남은 방정식에 대입합니다.
    3. 2단계에서 얻은 방정식을 풀고 한 변수의 값을 구합니다.
    4. 3단계에서 구한 변수의 값을 이용해 나머지 한 변수의 값을 구합니다.
  - 예시
    (1) $$x-2y=10$$
    (2) $$3x+y=5$$
    1. 1번 방정식을 $$x$$에 대해 푼 방정식 $$x=10+2y$$를 구합니다.
    2. 1단계에서 구한 $$x$$ 값을 2번 방정식에 대입한 식 $$3(10+2y)+y=5$$를 구합니다.
    3. 2단계 얻은 식을 통해 $$y$$ 해를 구합니다.<br>
    $$30+6y+y=5$$
    = $$7y=-25$$
    = $$y=\frac{25}{-7}$$
    4. 3단계에서 구한 변수 $$y$$의 해를 통해 변수 $$x$$의 해도 구합니다.<br>
    $$x-2(\frac{25}{-7})=10$$
    =$$x+\frac{50}{7}=10$$
    =$$x=\frac{20}{7}$$
- 소거법
  - 순서
    1. 한 방정식에 다른 방정식을 더하거나 빼는 방법으로 하나의 변수만을 가진 방정식을 구합니다.
    2. 1단계에서 구한 방정식을 통해 남은 변수의 해를 구합니다.
    3. 2단계에서 구한 변수값을 통해 나머지 한 변수의 해를 구합니다.
  - 예시
    (1) $$x-2y=10$$
    (2) $$3x+y=5$$
    1. 1번 방정식에 2번 방정식을 2배 곱한 값을 더해 $$y$$ 변수를 제거합니다.<br>
    $$x-2y+6x+2y=10+10$$
    =$$7x=20$$
    2. 1단계에서 구한 방정식을 통해 $$x$$의 해를 구합니다.<br>
    $$x=\frac{20}{7}$$
    3. 2단계에서 구한 변수 $$x$$의 값을 통해 변수 $$y$$의 해를 구합니다.<br>
    $$\frac{20}{7}-2y=10$$
    =$$-2y=10-\frac{20}{7}$$
    =$$-2y=\frac{50}{7}$$
    =$$y=-\frac{25}{7}$$
- 그래프 그리기
  - 순서
    1. 각 방정식을 그래프에 그린다.
    2. 방정식의 교차점을 구한다.
  - 예시
    - ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-그래프%20그리기%20예시.png)

### 변수와 방정식이 3개인 Linear System
- 순서
  1. 한 방정식을 이용해 남은 두 방정식에서 하나의 변수를 제거합니다.
  2. 남은 두 방정식은 두 개의 변수를 가지고 있으므로 변수와 방정식이 2개인 선형 연립 방정식이 됩니다. 따라서 같은 방식을 적용하여 두 변수의 해를 구합니다.
  3. 2단계에서 두 변수의 해를 구했으므로 주어진 방정식에 대입하여 나머지 한 변수의 해를 구합니다.
- 예시
  (1) $$x+y+z=10$$
  (2) $$2x-3y+5z=3$$
  (3) $$-x+y+2z=15$$
  1. 1번 방정식을 2번, 3번 방정식에 더하거나 빼서 변수 $$x$$를 제거한 방정식을 구합니다.<br>
  $$2x-3y+5z-2(x+y+z)=3-2(10)$$
  = $$-5y+3z=-17$$
  $$-x+y+2z+(x+y+z)=15+(10)$$
  = $$2y+3z=25$$
  2. 1단계에서 구한 두 방정식을 이용해 변수 $$y, z$$의 해를 구합니다.<br>
  $$-5y+3z-(2y+3z)=-17-(25)$$
  = $$-7y=-42$$
  = $$y=6$$<br>
  위 과정에서 $$y$$의 해는 6인걸 찾았으므로 이를 1단계에서 구한 두 방정식 중 하나에 대입하여 $$z$$의 해를 찾습니다.<br>
  $$2(6)+3z=25$$
  = $$12+3z=25$$
  = $$3z=13$$
  = $$z=\frac{13}{3}$$
  3. 2단계에서 변수 $$y, z$$의 해를 구했으므로 이를 처음 방정식 중 하나에 대입하여 $x$의 해를 구합니다.
  $$x+6+\frac{13}{3}=10$$
  = $$x=-\frac{1}{3}$$

### Matrix의 Dimension과 Entry
- Matrix는 숫자들이 직사각형 형태로 나열되어 있는 형태이다.
- Matrix dimensions
  - Matrix dimension은 보통 Row의 수와 Column의 수로 나타낸다.
  - Matrix의 Row와 Column의 수는 서로 같을 수도, 다를 수도 있다.
  - 예를 들어 Row가 3개이고 Column이 4개인 Matrix의 Dimension은 3⨉4로 나타낸다.
- Matrix entry
  - Matrix의 각 숫자들은 entry라고 한다.
  - 만약 Matrix의 Dimension이 3⨉4일 경우, 총 12개의 entry가 존재한다.
  - Matrix A의 k번째 Row의 l번째 Entry는 일반적으로 $$A_{k.l}$$ 형태로 표기한다.

### Matrix로 표현한 System
- 선형대수학에서 Matrix는 여러 방정식을 한 번에 표현하게 위해 사용한다.
- Matrix의 한 Row은 한 방정식을 나타낸다.
- Matrix의 한 Column은 한 변수를 나타낸다.
- Matrix에서 방정식의 결과값은 나타낼 수도, 나타내지 않을 수도 있다.
- Matrix에서는 $$x, y, z$$라는 변수를 $$x_1, x_2, x_3$$의 형태로 바꿔서 볼 수 있다.
- 예시
  (1) $$2x+3y+z=4$$
  (2) $$3x-2y+5z=-3$$
  (3) $$-5x+10z=-1$$<br>
  ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-행렬%20예시.PNG)
  ※ 위의 행렬은 방정식의 결과값을 포함한 행렬이다.

### 간단한 Row 연산
- 행렬식을 풀기 위해 행렬에 변화를 줄 수 있는 몇몇 방법이 존재한다.
- Row 순서 변환
  - 행렬의 Row 순서를 바꾸어도 각각의 방정식은 변하지 않으므로 결과에 영향을 주지 않는다
  - 예시
    - (1) $$3x+5y=6$$
    - (2) $$4x+y=1$$
    - (3) $$2x+7=-3$$
    - 위 3개의 방정식을 행렬로 나타낸 뒤 2행과 3행의 순서를 바꾼다고 해도 변수의 해에는 영향을 전혀 미치지 않는다.<br>
  ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-행%20순서%20변환%20예시.PNG)
- 특정 Row에 상수 곱하기
  - 행렬의 특정 Row에 상수를 곱해줘도 결국 해당 식에서 도출되는 해는 변하지 않으므로 결과에 영향을 주지 않는다.
  - 예시
    - (1) $$3x+5y=6$$
    - (2) $$4x+y=1$$
    - (3) $$2x+7=-3$$
    - 위 3개의 방정식을 나타낸 행렬에서 2번째 행에 2를 곱해주었다.
    - $$4x+y=1$$와 $$8x+2y=2$$는 동일한 방정식이므로 이러한 연산이 결과에 영향을 주지 않는다.
    ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-특정%20행에%20상수%20곱하기%20예시.PNG)
- 한 Row에 다른 Row를 더하기
  - 행렬의 특정 Row에서 다른 Row를 더하거나 빼도 결과에 영향을 주지 않는다.
  - 예시
    - (1) $$3x+5y=6$$
    - (2) $$4x+y=1$$
    - (3) $$2x+7=-3$$
    - 위 3개의 방정식을 나타낸 행렬에서 2번째 Row에 3번째 Row를 빼주었다. 
    - ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-한%20행에%20다른%20행%20더하기%20예시.png)

### Pivot Entry
- Pivot Entry란 각 Row에서 0이 아닌 첫 Entry
- Pivot Entry가 포함되어 있는 Column을 Pivot column이라고 한다.
- 예시<br>
  ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-피벗%20성분%20예시.png)
  - 만약 위와 같은 Matrix가 있다면 Pivot Entry은 각각 4, 2, -3이 된다.

### Row Echelon Form
- Row Echelon Form이란 성분이 계단 모양으로 배열된 행렬
- Row Echelon Form이 되기 위해서는 아래의 조건들을 만족해야함
  - 1. 모든 Pivot Entry는 1이어야한다.
  - 2. 모든 Entry가 0으로 이루어진 Row는 Matrix의 가장 아래에 있어야 한다.
  - 3. 각 Row의 Pivot Entry는 이전 Row의 Pivot Entry보다 오른쪽 Column에 있어야한다.(계단식 정렬)
- 예시<br>
  ![alt text](../Linear%20Algebra/images/선형대수학-단일%20행렬%20연산-행사다리꼴%20예시.png)
  - 위와 같이 각 Row의 Pivot Entry이 모두 1이어야함
  - 또한 각 Row의 Pivot Entry들이 계단 형식을 이루어져야함
- Reduced Row Echelon Form
  - 만약 Row Echelon Form의 각 pivot column에서 pivot entry를 제외한 모든 Entry가 0이라면 Reduced Row Echelon Form이다.<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Reduced%20Row%20Echelon%20Form-예시.png)
  - 위와 같이 각 Pivot Entry가 포함된 Column에서 Pivot Entry를 제외한 모든 Entry가 0인 경우, Reduced Row Echelon Form라고 할 수 있다.
  - Column 2의 Row 1이 -2가 있지만 해당 entry는 pivot entry가 아니므로 Column 2는 pivot column이 아님, 따라서 해당 Column과 상관 없이 Reduced Row Echelon Form이 됨

### Gauss-Jordan elimination
- Gauss-Jordan elimination은 Matrix를 Reduced Row Echelon Form으로 만드는 알고리즘
- 순서
  1. Matrix의 각 Row를 각각의 공통 인수를 이용해 수를 간단히 만들어 준다.(필수 과정은 아님)
  2. 만약 첫번째 Row의 첫 Entry가 0일 경우, 첫 Entry가 0이 아닌 다른 Row와 순서를 바꾼다.
  3. 첫번째 Row에 Row 연산을 적용해 첫 Entry를 1로 만들어줍니다.
  4. 첫번째 Row를 다른 Row에 더하거나 빼서 모든 Row의 첫 Entry를 0으로 만들어줍니다.
  5. Matrix가 Reduced Row Echelon Form이 될 때까지 2~4번 과정을 반복합니다.
- 예시<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%201.png)
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%202.png)
  - 가장 먼저 2번째 Row를 공통 인수인 5로 나누어줌(1번 과정)
  - Row 1의 Entry 1이 0이 아니므로 2번 과정은 생략<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%203.png)
  - Row 1에 -1을 곱해 Entry 1을 1로 만들어줌(3번 과정)
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%204.png)
  - Row 2에서 Row 1을 빼서 Entry 1을 0으로 만들어줌(4번 과정)<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%205.png)
  - Row 3에서 (2 ⨉ Row 1)을 빼서 Entry 1을 0으로 만들어줌(4번 과정)
  - 위 과정을 통해 Column이 1,0,0이 되었으니 이후 Row들에도 같은 연산을 적용<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%206.png)
  - Row 2를 4로 나누어 Entry2를 1로 만들어줌(3번 과정)<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%207.png)
  - Row 1에서 (5 ⨉ Row 2)를 빼서 Entry 2를 0으로 만들어줌(4번 과정)<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%208.png)
  - Row 3에서 (5 ⨉ Row 2)를 더해서 Entry 2를 0으로 만들어줌(4번 과정)<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%209.png)
  - Row 3에 -1을 곱해 Entry3을 1로 만들어줌(3번 과정)<br>
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Gause-Jordan%20elimination-예시%2010.png)
  - Row 1에 Row 3을 더해 Entry3을 0으로 만들어줌(4번 과정)
  - 위 과정을 통해 Matrix를 Reduced Row Echelon Form로 만들었음

### Number of solutions
- Solution이 하나인 경우
  - Matrix를 reduced row-echelon matrix로 만들었을 때 아래와 같은 형태로 만들 수 있으면 하나의 solution만 존재
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Numbers%20of%20solutions-Solution이%20하나인%20경우-예시.png)
- Solution이 없는 경우
  - Matrix를 reduced row-echelon matrix로 만들었을 때 아래와 같은 형태가 될 경우
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Numbers%20of%20solutions-Solution이%20없는%20경우-예시.png)
  - 변수 $$c != 0$$이라고 가정하면 $$0z = c$$가 되는데, 이 경우는 모순이 발생하므로 solution이 존재하지 않음
  - 만약 이런 경우가 발생할 경우 방정식들이 평행하다는 것을 의미(한  점에서 만나지 않는다)
- Solution이 무수히 많은 경우
  - Matrix를 reduced row-echelon matrix로 만들었을 때 아래처럼 0만 존재하는 행이 있을 경우
  ![alt text](../Linear%20Algebra/images/Linear%20Algebra-Operations%20on%20one%20matrix-Numbers%20of%20solutions-Solution이%20무수히%20많은%20경우-예시.png)
  - $$0z=0$$은 모든 $$z$$에 대해 성립하므로 solution이 무수히 많이 존재