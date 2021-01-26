### **Sprint 1**
***

**Day 1**

**EDA - Exploratory Data Analysis : 데이터 전처리** 

데이터프레임 열과 행 내부의 데이터 편집, 결측치 대체 등
***

**Day 2**

**Feature Engineering  : feature들을 재조합하여 새로운 feature를 만드는 과정**

데이터프레임의 열과 행의 연산을 위해 데이터 타입을 통일하는 과정이 필요
***

**Day 3**

**Data Manipulation : 데이터 조합** 

- concat : 단순히 두 개의 데이터프레임을 열이나 행 방향으로 이어 붙이는 것
- merge : 두 개의 데이터프레임에서 공통된 부분을 찾아 그 부분을 중심으로 데이터를 이어붙이는 것 → sql의 join과 비슷
- conditioning : 데이터 조합 시에 원하는 부분만 뽑아 이어 붙일 수 있도록 조건을 지정하는 과정 - 필터링 → isin, groupby 등을 이용
- tidy한 데이터를 위해 melt 함수를 이용 → melt와 반대 역할 - pivot_table
