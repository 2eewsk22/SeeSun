# 🏆 [Interview-Go] : AI 기반 면접 & 코딩테스트 학습 플랫폼

![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5.9-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![React](https://img.shields.io/badge/React-19.2.3-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2-Ubuntu_24.04-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)

## 📖 프로젝트 소개
> **"취업 준비생을 위한 올인원 학습 파트너"** > 유튜브 추천 영상, 실시간 채용 공고, AI 모의 면접, 코딩 테스트 연습을 한곳에서 제공하는 웹 서비스입니다.

* **개발 기간:** 2025.12.15 ~ 2026.01.09 (약 4주)
* **개발 인원:** 총 5명

<br>

## 1. 🚩 개발 배경 및 목적 (Background & Purpose)
최근 취업 시장의 경쟁이 심화됨에 따라 면접의 중요성이 그 어느 때보다 커졌으며, 이에 따라 취업 준비생들은 면접 대비를 위해 막대한 시간과 경제적 비용을 투입하고 있습니다.

하지만 전문 취업 컨설팅은 구직자에게 부담이 될 정도의 고비용으로 접근성이 떨어지고, 대안으로 선택되는 면접 스터디는 팀원들의 주관적이고 비전문적인 의견에 의존할 수밖에 없어 답변의 질적 개선을 기대하기 힘든 실정입니다.

본 프로젝트는 이러한 문제점을 해결하기 위해 **비용 부담 없이 시공간의 제약 없이 전문적인 피드백을 받을 수 있는 AI 기반 면접 솔루션**을 구축하게 되었습니다.

<br>

## 2. 🛠 개발 환경 (Tech Stack)

### 🖥 Backend
| 기술 | 버전/설명 |
| :--- | :--- |
| **Language** | Java 21 |
| **Framework** | Spring Boot 3.5.9 |
| **ORM** | Spring Data JPA |
| **Database** | MySQL 8.0 |
| **Library** | Lombok 1.18.42 |

### 🎨 Frontend
| 기술 | 버전/설명 |
| :--- | :--- |
| **Language** | JavaScript, HTML5, CSS3 |
| **Library** | React 19.2.3 |
| **Runtime** | Node.js 24.12.0 |
| **Module** | react-youtube, WordCloud |

### 🤖 AI & Data
| 기술 | 버전/설명 |
| :--- | :--- |
| **Language** | Python 3.9 |
| **API** | Google Gemini API (생성형 AI) |
| **H/W Acceleration** | CUDA 12.8 (GPU 가속) |

### ⚙️ Infra & Tools
* **Server:** AWS EC2 (Ubuntu 24.04)
* **IDE:** Eclipse STS 4.32.2
* **VCS:** Git, GitHub, SourceTree

<br>

## 3. 🏗 시스템 구성 및 아키텍처 (Architecture)

본 프로젝트는 사용자의 요청을 처리하는 Spring Boot 백엔드와 동적 UI를 제공하는 React 프론트엔드로 구성되며, 다양한 외부 API를 활용하여 서비스를 확장했습니다.

### ✅ Core Components
1. **JDK 21**: 최신 자바 런타임 환경 구성
2. **Spring Boot 3.5.9**: 비즈니스 로직 처리 및 REST API 서버 구축
3. **Spring Data JPA**: DB 객체 매핑 및 효율적인 데이터 관리
4. **MySQL 8.0**: 회원 정보, 학습 기록, 피드백 데이터 저장소
5. **React 19.2.3**: 사용자 중심의 컴포넌트 기반 UI 구축
6. **Node.js 24.12.0**: 프론트엔드 빌드 및 실행 환경
7. **AWS EC2**: 클라우드 서버 배포 및 운영
   
### ✅ External APIs
8. **Google Gemini API**: 사용자 답변 분석 및 맞춤형 피드백 생성
9. **Naver Search API**: 실시간 채용 트렌드 검색어 수집
10. **YouTube Data API**: 면접 꿀팁 및 기업 분석 영상 큐레이션
11. **react-youtube**: 웹 내 영상 플레이어 임베딩
12. **고용24 Open API**: 실시간 공공 채용 공고 연동

<br>

## 4. ✨ 주요 기능 (Key Features)

### 🔓 Public Services (비회원 기능)
로그인 없이도 최신 취업 트렌드를 파악하여 서비스 유입을 유도합니다.

* **☁️ 취업 워드 클라우드:** Naver API 분석을 통해 현재 채용 시장에서 가장 핫한 키워드를 시각적으로 제공
* **📋 실시간 채용 공고:** 스케줄러를 적용하여 고용24 데이터를 실시간으로 갱신 및 리스트업
* **📺 추천 영상 큐레이션:** 면접 팁, 직무 분석 등 유익한 영상을 카테고리별로 추천 제공

### 🔐 Private Services (회원 기능)
본격적인 취업 역량 강화를 위한 핵심 훈련 기능입니다.

* **🤖 AI 모의 면접**
    * **몰입형 환경:** 면접 시작 시 주변 요소를 제거하여 면접에 집중할수 있는 분위기 조성
    * **이탈 방지 UX:** 훈련 완주를 위해 별도의 종료 절차를 거치도록 설계
    * **상세 피드백:** 면접 종료 즉시 AI가 답변의 논리성/적합성을 분석한 리포트 제공 및 마이페이지 자동 저장

* **💻 역량 테스트 (Coding & CS)**
    * **챕터별 학습:** 개발자 필수 CS 지식 및 알고리즘 문제 풀이 제공
    * **실시간 채점:** 답안 제출 시 데이터 무결성을 검증하며 즉시 채점 결과 제공
    * **학습 관리:** 상단 내비게이션을 통해 언제든 학습 진척도 확인 가능

<br>

## 5. 👨‍💻 팀원 소개 (Team Members)

| 이름 | 담당 역할 (Role) | GitHub |
| :---: | :--- | :---: |
| **이원석 (Team Leader)** | 프로젝트 총괄, 유튜브/채용공고/워드클라우드 구현 | [@이원석](https://github.com/2eewsk22) |
| **권민성** | 회원가입/로그인(Auth), 계정 보안 로직, 아이디/비번 찾기 | [@권민성](https://github.com/aaaaa-113) |
| **김원혁** | 프로젝트 아키텍처, AI 면접 로직, DB 설계, AWS 배포 | [@김원혁](https://github.com/kwork9237) |
| **김지민** | 전체 UI/UX 설계, 공통 컴포넌트, 마이페이지(활동 기록) | [@김지민](https://github.com/kimjimin08) |
| **조윤** | 코딩 테스트(CS/Algorithm) 로직 구현, 문제 풀이 및 채점 시스템 | [@조윤](https://github.com/joyoon2) |


<br>

## 6. 📸 스크린샷 (Screenshots)

| 메인 페이지 (Main) | 워드 클라우드 (Word Cloud) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/3deca42e-37dc-44c4-aaab-65abc9a7dea6" width="400" alt="메인페이지"> | <img src="https://github.com/user-attachments/assets/161a2c78-07da-428a-9643-5ab2b1f68d64" width="400" alt="워드클라우드"> |

| 추천 영상 (YouTube) | 실시간 채용 공고 (Job List) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/ec82aaab-a02a-4538-8e19-e8104ce4325f" width="400" alt="추천영상"> | <img src="https://github.com/user-attachments/assets/50d5f27d-3348-4ab3-978e-6df98b1a7229" width="400" alt="채용공고"> |

| AI 모의 면접 (AI Interview) | 역량 테스트 (Coding Test) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/c8845f1f-dfe4-4071-b279-bf19d7fbde44" width="400" alt="AI면접"> | <img src="https://github.com/user-attachments/assets/5d684cb9-8d74-43f4-956e-bf6a61857f0b" width="400" alt="코딩테스트"> |

| 마이 페이지 (My Page) |
| :---: |
| <img src="https://github.com/user-attachments/assets/6450255c-b142-42fc-b30a-defd5b5a70ca" width="800" alt="마이페이지"> 


<br>

## 7. 🚀 트러블 슈팅 (Trouble Shooting)

### ⚡️ IFrame 렌더링 최적화 및 비동기 오류 해결 
추천 영상 페이지에서 다수의 영상 컴포넌트를 처리하며 발생한 성능 저하 및 에러를 해결.

### ⚠️ 문제 발생 (Issue)

렌더링 성능 저하: 한 화면에 다수의 IFrame 영상이 동시에 로드되면서 초기 렌더링 시간이 길어짐.

비동기 처리 충돌: 영상 로딩 중 헤더 탭을 빠르게 전환할 경우, 컴포넌트 마운트/언마운트 과정에서 비동기 처리 오류 발생.

### 🛠 해결 전략 (Solution)

썸네일 우선 노출: 초기 진입 시 무거운 IFrame을 바로 생성하지 않고, DB에 저장된 영상 ID를 활용해 썸네일 이미지와 재생 버튼만 먼저 렌더링하도록 변경.

Lazy Loading (지연 로딩) 적용: 사용자가 실제 재생 버튼을 클릭하는 시점에 영상 컴포넌트를 마운트하고 데이터를 요청하도록 로직 개선.

### ✅ 결과 및 배운점 (Result)

성능 최적화: 불필요한 리소스 낭비를 막고 초기 화면 로딩 속도를 획기적으로 개선.

안정성 확보: 비동기 로딩 중 이동 시 발생하던 오류를 해결하여 안정적인 UX 제공.

Insight: "무조건적인 데이터 로딩보다 사용자의 요청 시점에 필요한 만큼 로드하는 것이 성능 최적화의 핵심"임을 이해.
