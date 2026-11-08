# AI 기반 데이터 분석 자동화 범위 및 한계 탐구 (LAMBDA Agent 벤치마크)

> **PBL 과제/문제 상황**: 실제 데이터 분석 과정의 AI 활용과 어느 단계까지 자동화가 가능한지에 대한 탐구  
> **PBL 학습 목표**: 빅데이터 시대에 주목받고 있는 AI 기술이 데이터 분석 과정에 어떻게 적용되고 있으며, 데이터 분석 자동화의 범위와 한계를 조사한다.

---

## 📋 1. 계획서 ↔ 논문(LAMBDA) 및 실행 전략 매핑

| 번호 | 학습과제 (Learning Issues) | 연구 및 조사계획 / 역할분담 (Action Plans) | 논문(LAMBDA) 연계 및 실습 구현 방법 |
| :-: | :--- | :--- | :--- |
| **1** | 데이터 분석 기본 단계(수집, 전처리, 시각화, 모델링 등)의 개념과 흐름 학습 | 데이터 분석 단계 및 AI 활용 사례 관련 문헌/기사/기술블로그/논문 조사 | • 데이터 분석 5대 파이프라인 정립  <br>• LAMBDA의 표준 데이터 분석 로직(데이터 탐색 $\rightarrow$ 전처리 $\rightarrow$ EDA $\rightarrow$ 모델링 $\rightarrow$ 리포팅) 분석 |
| **2** | 생성형 AI 및 데이터 분석 AI 도구(ChatGPT, Claude 등)의 활용 방식 조사 | AI 기반 데이터 분석 도구 기능 및 자동화 범위 비교 분석표 작성 | • ChatGPT(Code Interpreter), Claude, OpenInterpreter 대 **LAMBDA(Multi-Agent + Knowledge Base)** 비교<br>• 기능 및 자동화 범위 비교 분석표 작성 |
| **3** | AI의 자동화 범위(자동 전처리, 자동 코드 생성, Auto-EDA 등) 파악 | 공개 기초 데이터셋(Kaggle 등) 활용 AI 도구 자동화 시연 및 정확성 관찰 | • **직접 시연 파트**: Wine/Iris/Framingham 등 벤치마크 데이터셋 활용<br>• Single Agent 대 Multi-Agent(Programmer+Inspector) 자가 수정(Self-Correction) 정확도 테스트 |
| **4** | AI 데이터 분석 자동화 적용 분야(금융, 마케팅, 헬스케어 등) 및 응용 사례 학습 | 수집 문헌과 직접 시연 결과를 종합하여 AI 자동화 현주소 및 발전 방향 도출 | • 헬스케어/의학(AIDS, NHANES, Breast Cancer, Genomic datasets) 등 논문의 실제 적용 도메인 사례 분석<br>• AI 분석 자동화의 산업별 현주소 도출 |
| **5** | AI 분석 자동화 한계점(보안, 통계적 오류, 인간 판단 필요성 등) 파악 | 수집 자료 및 시연 결과 팀원 토의 진행 및 외부 피드백 보완 | • **보안**: 클라우드 API 보안 위험 vs 로컬/오픈소스 LAMBDA<br>• **통계 오류/도메인 미스매치**: 미스매치 시 툴 직접 사용 오류 사례 분석<br>• **Human-in-the-loop**: 인간 개입 필요성 도출 |
| **6** | 학부생 수준 AI 데이터 분석 자동화 도구의 장단점 정리 | 최종 조사 내용 바탕 보고서 작성 및 발표용 PPT 제작 | • 학부생 관점 AI 도구 장단점 가이드라인 작성<br>• 자동 생성 리포트(LAMBDA Report Generation 기능 참고) 및 최종 보고서/PPT 완성 |

---

## 📅 2. 주차별 한 학기 수행 로드맵 (1~16주차)

### 🚀 1단계: 데이터 분석 파이프라인 및 AI 도구 이론 조사 (1~4주차)
* **[학습과제 1 & Action Plan 1]**
  * 데이터 분석 표준 5단계(수집 $\rightarrow$ 전처리 $\rightarrow$ EDA/시각화 $\rightarrow$ 머신러닝 모델링 $\rightarrow$ 리포팅)의 흐름과 개념 학습.
  * 학술 기사, IT 기술 블로그, 관련 논문(LAMBDA 등) 조사 진행.
* **[학습과제 2 & Action Plan 2]**
  * ChatGPT(Code Interpreter), Claude, OpenInterpreter, TaskWeaver, LAMBDA 등 다양한 AI 데이터 분석 도구의 작동 방식 조사.
  * 도구별 아키텍처(Single-Agent vs Multi-Agent) 및 데이터 처리 메커니즘 차이 분류.

---

### 🧪 2단계: 데이터셋 가공 및 AI 도구별 실습 시연 (5~9주차)
* **[학습과제 3 & Action Plan 3]**
  * **실험용 공공/Kaggle 데이터셋 준비**:
    1. **기본 범주형/회귀 데이터**: Iris, Wine, Abalone
    2. **결측치(Missing Data) 포함 데이터**: Framingham Heart Study
  * **AI 도구별 자동화 시연 및 정확성 비교 테스팅**:
    * **자동 전처리 및 Auto-EDA**: 자연어 지시만으로 변수 인코딩, 스케일링, 상관관계 히트맵 및 상관계수 행렬을 생성하는지 검증.
    * **자가 오류 수정(Self-Correction) 시연**: 결측치나 문자열 데이터 입력 시 발생하는 에러 로그를 AI가 스스로 읽고 코드 수정(Programmer $\leftrightarrow$ Inspector 피드백 고리)을 완수하는지 확인.
    * **모델링 및 교차검증**: Logistic Regression, SVM, Random Forest, XGBoost 등 모델 학습과 GridSearchCV 성능 산출 자동화 시연.

---

### 📊 3단계: 도구 비교표 작성, 사례 분석 및 한계점 도출 (10~12주차)
* **[학습과제 4 & Action Plan 4]**
  * 헬스케어(AIDS Clinical Trials, Genomic datasets), 제조(Concrete Compressive Strength), 비즈니스 등 AI 데이터 분석 자동화가 적용되는 대표 분야 응용 사례 정리.
  * 직접 시연 결과와 문헌 자료를 결합하여 현재 AI 자동화 기술의 현주소 도출.
* **[학습과제 5 & Action Plan 5]**
  * **AI 데이터 분석 자동화 한계점 3대 분석**:
    1. **데이터 보안 및 프라이버시**: 외부 서버 전송 문제(ChatGPT) vs 로컬 구축형(LAMBDA) 비교.
    2. **통계적 오해석 및 Misalignment 오류**: 지시문과 도구/손실함수(Loss function)가 어긋났을 때 AI가 검증 없이 기존 코드를 그대로 실행하는 한계 분석.
    3. **인간 판단의 필요성 (Human-in-the-Loop)**: 완전 자동화의 위험성과 사용자 직접 수정/개입 인터페이스의 필수성 도출.
  * 팀원 간 토의 진행 및 지도교수/외부 피드백을 반영하여 내용 보완.

---

### 📝 4단계: 종합 분석 정리, 보고서 작성 및 발표 (13~16주차)
* **[학습과제 6 & Action Plan 6]**
  * **학부생 관점의 AI 데이터 분석 도구 장단점 종합 비교표 작성**:
    * 단일 Prompt 기반 LLM vs Multi-Agent 기반 데이터 에이전트의 처리 속도, 토큰 소모량, 자가 수정율, 보안성 등 정리.
  * 최종 실습 결과물, 리포트 시각화 자료를 종합하여 **최종 과제 수행 보고서 작성 및 발표용 PPT 제작**.

---

## 👥 3. 팀원 역할 분담

**팀명**: 통계1  
**팀원**: 김채원, 김성원, 오성훈, 정윤찬, 엄인영

| 팀원 이름 | 계획서상 담당 영역 | 주요 세부 수행 내용 |
| :---: | :--- | :--- |
| **김채원** | **AI 도구 조사 및 시연 총괄** | • ChatGPT, Claude 등 주요 생성형 AI 데이터 분석 도구 사례 및 기능 조사 (학습과제 2, 3)<br>• 도구별 데이터 분석 단계별 자동화 범위 비교 분석표 작성 주도 (Action Plan 2) |
| **김성원** | **Multi-Agent 분석 & 테스팅 주도** | • LAMBDA 논문의 Multi-Agent(Programmer-Inspector) 및 Self-Correction 구조 분석 (학습과제 2, 3)<br>• Kaggle/공공 데이터셋 대상 도구별 자가 오류 수정 및 모델링 자동화 시연 실행 (Action Plan 3) |
| **오성훈** | **데이터 수집 & 파이프라인 실습** | • 데이터 분석 5대 단계 개념 정리 및 학술/기술 기사 조사 (학습과제 1, Action Plan 1)<br>• 실습용 데이터셋(Tabular, Missing Data) 수집 및 시연 결과의 통계적 정확성 검증 (Action Plan 3) |
| **정윤찬** | **응용 분야 조사 & 한계점 분석** | • AI 분석 자동화의 산업별(헬스케어, 금융 등) 대표 응용 사례 수집 (학습과제 4, Action Plan 4)<br>• 보안 이슈, 통계적 오류, Human-in-the-loop 필요성 정리 및 팀 토의 보완 (학습과제 5, Action Plan 5) |
| **엄인영** | **결과 종합, 보고서 및 PPT 제작** | • 학부생 관점 AI 자동화 도구 장단점 가이드라인 최종 정리 (학습과제 6)<br>• 시연 캡처 및 수집 자료 통합, 최종 보고서 작성 및 발표용 PPT 제작 총괄 (Action Plan 6) |