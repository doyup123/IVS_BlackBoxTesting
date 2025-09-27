자동화 테스팅을 통한 BlackBox Testing (동적검증 CANoe/CAPL)
=====================
|이름|프로젝트 기간|역할|
|---|------------|------|
|김도엽|2025.04~2025.05|개인 프로젝트|

## 프로젝트 개요
요구사양서를 분석하고 Vector CANoe를 활용해 테스트 환경을 구축해 고장 진단 제어기의 결함을 검증하는 프로젝트 



## 검증 Concept
<img width="1051" height="331" alt="검증컨셉" src="https://github.com/user-attachments/assets/57a25080-601e-4f84-8f49-2c3493699bb3" />

## 검증 단계
<img width="673" height="187" alt="검증 단계" src="https://github.com/user-attachments/assets/8f234d71-313f-4a29-9963-f273f7eee47e" />

### 1. 요구사양서 분석
#### 1.1 CAN 통신사양서 분석 및 CAN DB 작성
| 구분 | 이미지 |
|------|--------|
| CAN 통신사양서 | ![CAN 통신사양서](https://github.com/user-attachments/assets/4aa13ded-cf38-4a3a-9ec8-c80574a586dc) |
| CAN DB 작성 | ![CANDB](https://github.com/user-attachments/assets/31dc7fbe-904b-47d3-ac74-74f4dc499e1c) |





| TC ID | 목적           | 사전조건               | 입력 시나리오                           | 기대 결과                        | 실제 관찰 결과                | 판정       |
| ----- | ------------ | ------------------ | --------------------------------- | ---------------------------- | ----------------------- | -------- |
| TC-01   | 검출 경계 하한-ε   | Engine=Run, IGN=On | Batt% **14.9**를 **5s** 유지         | **4.9~5.1s** 내 Fault Level=2 | Fault=2 미발생             | **Fail** |
| TC-02   | 검출 경계값(=15%) | Engine=Run, IGN=On | Batt% **15.0**을 **5s** 유지         | **4.9~5.1s** 내 Fault Level=2 | Level=0 유지(미검출)         | **Fail** |
| TC-03   | 검출 경계 상한+ε   | Engine=Run, IGN=On | Batt% **15.1**을 **6s** 유지         | Fault 미발생                    | 미발생                     | **Pass** |
| TC-04   | 검출 타이밍–조기    | Engine=Run, IGN=On | **14.0%** 진입 후 **4.8s**만 유지       | **4.9s 이전** Fault 금지         | 미발생                     | **Pass** |
| TC-07   | 회복 경계 하한-ε   | Fault=2 상태 유지      | Batt% **29.9**로 상승, **200ms** 관찰  | 회복 불가(2 유지)                  | **Voltage 0.01V**에서만 회복 | **Fail** |
| TC-08   | 회복 경계값(=30%) | Fault=2 상태 유지      | Batt% **30.0**으로 상승, **200ms** 관찰 | **90~110ms** 내 2→1           | Voltage 조건에서만 회복        | **Fail** |
| TC-09   | 회복 경계 상한+ε   | Fault=2 상태 유지      | Batt% **30.1**로 상승, **200ms** 관찰  | **90~110ms** 내 2→1           | Voltage 조건에서만 회복        | **Fail** |
