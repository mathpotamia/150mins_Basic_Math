# 📊 데이터 분석: 관계의 세기를 측정하는 방법  

## ✨ 1. 관계의 세기 측정 (산포도)  
- **두 변수(예: 공부 시간과 시험 점수) 간의 관계**를 파악하는 가장 간단한 방법은 **산포도(Scatter Plot)**를 그리는 것.  
- 산포도를 통해 데이터의 분포를 시각적으로 확인할 수 있으며, **어느 정도의 관계가 있는지 대략적으로 판단 가능**함.  
- 하지만 산포도만으로 **정확한 관계의 세기를 수치화할 수 없음**, 따라서 **상관계수(Correlation Coefficient)** 개념이 필요함.

---

## 📈 2. 상관계수 (Correlation Coefficient)  
- **상관관계의 유형**  
  1. **양의 상관관계 (Positive Correlation)**:  
     - 공부 시간이 늘어날수록 시험 점수가 증가하는 경우  
     - 상관계수 값이 **+1에 가까울수록 강한 양의 상관관계**  
  2. **음의 상관관계 (Negative Correlation)**:  
     - 공부 시간이 늘어날수록 시험 점수가 감소하는 경우  
     - 상관계수 값이 **-1에 가까울수록 강한 음의 상관관계**  
  3. **상관관계 없음 (No Correlation)**:  
     - 두 변수 간 **거의 아무런 관계가 없을 경우**  
     - 상관계수 값이 **-0.3 ~ +0.3** 사이  

---

## 🔢 3. 상관계수 계산 방법  
### ✅ Step 1: 평균과 표준편차 계산  
- 각 데이터의 **평균(Mean)**과 **표준편차(Standard Deviation)**을 구함.  
  - 예제 데이터에서:  
    - 평균 공부 시간 = **11시간**, 표준편차 = **6**  
    - 평균 점수 = **60점**, 표준편차 = **20**  

### ✅ Step 2: 편차 계산  
- 각 학생의 **(공부 시간 - 평균)** 값과 **(점수 - 평균)** 값을 구함.  

### ✅ Step 3: 곱셈  
- 각 편차를 서로 곱한 값을 계산하여 합산.  

### ✅ Step 4: 평균 계산  
- Step 3에서 계산한 값들의 **평균을 구함**.  

### ✅ Step 5: 표준편차로 나누기  
- Step 4에서 구한 값을 **(공부 시간의 표준편차 × 점수의 표준편차)**로 나누어 **상관계수 값**을 도출함.  

💡 **결과**  
- 예제 데이터에서 상관계수 값 = **0.78**  
  → 즉, **공부 시간과 시험 점수 간에는 강한 양의 상관관계가 있음.**  

---

## 🎯 4. 추가로 공부하면 좋을 개념(GPT추천)    
🔍 **추가 개념 학습**  
- **공분산(Covariance)**: 상관계수와 밀접한 개념으로, 두 변수 간 관계를 계산하는 기초적인 지표.  
- **피어슨 상관계수(Pearson Correlation Coefficient)**: 가장 일반적으로 사용되는 상관계수 공식.  
- **스피어만 상관계수(Spearman Rank Correlation)**: 두 변수 간 **순위(rank)**를 비교하여 상관관계를 분석하는 방법.  
- **상관과 인과관계의 차이**: 상관관계가 있다고 해서 반드시 인과관계(원인과 결과 관계)가 성립하는 것은 아님.  

📌 **추가 실습 추천**  
- **Python을 활용한 상관계수 계산 실습**  
  ```python
  import numpy as np

  # 공부 시간 & 시험 점수 데이터
  study_time = np.array([10, 12, 2, 7, 21, 19, 11, 6])
  scores = np.array([80, 50, 50, 40, 90, 80, 60, 30])

  # 상관계수 계산
  correlation = np.corrcoef(study_time, scores)[0, 1]
  print(f"상관계수: {correlation:.2f}")
  ```
  → `numpy.corrcoef()`를 사용하면 손쉽게 상관계수를 계산할 수 있음.

---

## 📌 정리  
1. **산포도**를 그려 데이터의 분포를 시각적으로 확인.  
2. **상관계수**를 계산하여 변수 간 관계의 강도를 수치로 표현.  
3. **상관계수 값이 +1에 가까우면 강한 양의 상관관계, -1에 가까우면 강한 음의 상관관계**를 가짐.  
4. **Python을 활용하여 직접 상관계수를 계산해보며 개념을 체화할 것!** 🚀  