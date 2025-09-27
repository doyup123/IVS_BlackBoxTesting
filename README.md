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

## 고장 진단 제어기 요구사항
<img width="600" height="364" alt="image" src="https://github.com/user-attachments/assets/3271ac23-075c-4128-b721-de8dd199b1cc" />

------------------------

### 1. 요구사양서/요구사항서 분석 🔎
#### 1.1 CAN 통신사양서 분석 및 CAN DB 작성
| 구분 | 이미지 |
|------|--------|
| CAN 통신사양서 | ![CAN 통신사양서](https://github.com/user-attachments/assets/4aa13ded-cf38-4a3a-9ec8-c80574a586dc) |
| CAN DB 작성 | ![CANDB](https://github.com/user-attachments/assets/31dc7fbe-904b-47d3-ac74-74f4dc499e1c) |
| 분석 단계에서 결함 발견|<img width="1107" height="663" alt="요구사항 분석시 결함 발견" src="https://github.com/user-attachments/assets/9cabbbb0-e476-49dc-955d-a18126635236" /> |
|결함 조기 보고|<img width="1080" height="456" alt="검증 보고서 (요구사항 분석)" src="https://github.com/user-attachments/assets/96d62afd-2c8d-4db6-bbeb-e5482ba6b2d6" />|

#### 1.2 요구사항서 분석 및 TestCase 작성
| 구분 | 이미지 |
|------|--------|
|요구사항 분석| <img width="816" height="319" alt="요구사항 분석" src="https://github.com/user-attachments/assets/705106ab-cb1b-4060-be55-3791a919523a" /> |
|테스트케이스 작성| <img width="1171" height="175" alt="image" src="https://github.com/user-attachments/assets/e150ffe9-3e50-4e72-9098-e6b23f090c4f" /> |

### 2. 검증환경 구축 🔨
| 구분 | 이미지 | 
|------|--------|
|시뮬레이션 환경 셋업| <img width="937" height="537" alt="시뮬레이션 셋업" src="https://github.com/user-attachments/assets/3ee6954e-a2b1-45e2-a95c-abe368786407" /> |
|수동 검증을 위한 UI|<img width="1197" height="657" alt="UI" src="https://github.com/user-attachments/assets/c1c34c36-7a14-49e5-8ac3-cfe765a01190" /> |
|자동화 스크립트 작성| <img width="722" height="582" alt="image" src="https://github.com/user-attachments/assets/e245301a-6f9d-4192-978a-061d8360c61d" /> |

### 3. 검증  수행

#### 3.1 자동화 스크립트 결과 보고
<img width="1436" height="383" alt="자동화 스크립트 결과 보고" src="https://github.com/user-attachments/assets/a8b73400-55f1-4faf-a76e-56cc94727901" />

#### 3.2 CAN Message 분석을 통한 결함 확인
<img width="766" height="537" alt="캔 메세지" src="https://github.com/user-attachments/assets/6bc0eda6-e10d-4e5e-acf3-9e6c9375cd93" />

### 4. 검증 결과 분석 및 보고
<img width="1264" height="521" alt="경계값 분석 결과보고" src="https://github.com/user-attachments/assets/7405fe7c-4616-4664-b7af-ddf5713ff594" />







