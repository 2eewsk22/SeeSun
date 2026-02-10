# 🏆 [SeeSun] : WebRTC 기반 실시간 멘토링 플랫폼

![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5.9-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![React](https://img.shields.io/badge/React-19.2.3-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2-Ubuntu_24.04-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)

## 📖 프로젝트 소개
> SeeSun은 기존 온라인 멘토링의 한계인 '도구의 파편화'와 '지연 시간'을 해결하기 위해 개발된 WebRTC 기반 올인원 화상 멘토링 플랫폼입니다.
> 강의 개설, 수강 신청, 결제, 그리고 실시간 화상 수업까지 끊김 없는 경험을 제공합니다.

* **개발 기간:** 2026.01.12 ~ 2026.02.10 (약 4주)
* **개발 인원:** 총 6명

<br>

## 1. 🚩 개발 배경 및 목적 (Background & Purpose)
기존 온라인 멘토링 시장은 영상, 자료 공유, 채팅 등 도구가 분리되어 있어 실시간 상호작용이 비효율적이었습니다. 특히 회화 및 코칭 분야에서는 미세한 지연과 끊김 현상으로 인해 학습 효과가 저하되는 문제가 있었습니다.

본 프로젝트는 이러한 문제를 해결하기 위해 WebRTC 기술을 도입하여 저지연·양방향·통합형 멘토링 환경을 구축하고, 멘토와 멘티 간의 상호작용을 통해 대면 멘토링 수준의 경험을 제공하는 것을 목적으로 합니다.

<br>

## 2. 🛠 개발 환경 (Tech Stack)

### 🖥 Backend
| 기술 | 버전/설명 |
| :--- | :--- |
| **Language** | Java 21 |
| **Framework** | Spring Boot 3.5.9 |
| **Mapper** | MyBatis |
| **Database** | MySQL 8.0 |
| **Library** | Lombok 1.18.42 |

### 🎨 Frontend
| 기술 | 버전/설명 |
| :--- | :--- |
| **Language** | JavaScript, HTML5, CSS3 |
| **Library** | React 19.2.3 |
| **Media** | WebRTC (Janus Gateway 연동 |
| **payment** | Toss Payments SDK |


### ⚙️ Infra & Tools
* **Server:** AWS EC2 (Ubuntu 24.04)
* **VCS:** Git, GitHub, SourceTree
* **Collaboration:** Notion, slack

<br>

## 3. 🏗 시스템 구성 및 아키텍처 (Architecture)

본 프로젝트는 React 프론트엔드와 Spring Boot 백엔드로 구성되며, WebRTC 미디어 서버를 통해 실시간 화상 통신을 중계합니다.

### ✅ Core Components
1. **JDK 21**: 최신 자바 런타임 환경 구성
2. **Spring Boot**: REST API 서버 및 비즈니스 로직 처리
3. **MyBatis**: DB 객체 매핑 및 조작
4. **MySQL 8.0**: 회원 정보, 강의 데이터, 결제 내역
5. **React 19.2.3**: 사용자 중심의 컴포넌트 기반 UI 구축
6. **Node.js 24.12.0**: 프론트엔드 빌드 및 실행 환경
7. **AWS EC2**: 클라우드 서버 배포 및 운영
   
### ✅ External Service
8. **WebRTC (Janus)**: 실시간 화상, 음성, 화면 공유 스트리밍 처리
9. **Toss Payments**: 강의 수강 신청을 위한 결제 시스템 연동
10. **WebSocket/SSE**: 실시간 채팅 처리

<br>

## 4. ✨ 주요 기능 (Key Features)

### 🔓 Public Services
* **강의 탐색:** 개설된 멘토링 강의 목록 및 상세 정보 확인
* **회원가입/로그인:** 멘토, 멘티, 관리자 권한별 회원가입 및 로그인

### 🔐 Private Services (회원 기능)

* **📹 실시간 화상 강의 (WebRTC)**
    * **강의실:** 멘토(Host)와 멘티(Guest) 간 1:1 회상 연결
    * **상호작용:** 카메라/마이크 제어, 화면 공유, 실시간 채팅 기능
    * **자동 관리:** 강의 종료 시 리소스 자동 Cleanup 및 퇴장 처리
      
* **💳 강의 관리 및 결제**
    * **멘토:** 강의 개설, Q&A 답변
    * **멘티:** 수강 신청, 결제(Toss), 마이페이지 내 수강 내역 관리
    * **관리자:** 멘토 승인/반려, 신고 누적 강의 관리, 회원 제재

<br>

## 5. 👨‍💻 팀원 소개 (Team Members)

| 이름 | 담당 역할 (Role) | GitHub |
| :---: | :--- | :---: |
| **이원석 (Team Leader)** | 프로젝트 총괄, 결제 API, 마이페이지 구현 | [@이원석](https://github.com/2eewsk22) |
| **권민성** | 관리자 기능, 공지사항 | [@권민성](https://github.com/aaaaa-113) |
| **김원혁** | 요구사항 분석, DB 설계, AWS 배포, 파일 시스템 | [@김원혁](https://github.com/kwork9237) |
| **김지민** | UI/UX 설계, 메인 페이지, 공통 컴포넌트 제작 | [@김지민](https://github.com/kimjimin08) |
| **조 윤** | 강의 목록/상세/개설 페이지 설계 및 구현 | [@조윤](https://github.com/joyoon2) |
| **홍진기** | WebRTC 설계/테스트, 화면 공유/녹화, 실시간 채팅 | [@홍진기](https://github.com/Bmer2020) |


<br>

## 6. 📸 스크린샷 (Screenshots)

| 메인 페이지 (Main) | 화상 강의실 (WebRTC) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/b92d4236-aaee-4c17-9e1d-9abb408218c0" width="400" alt="메인페이지"> | <img src="https://github.com/user-attachments/assets/a56e6a4e-cf93-4cae-93bc-d64cd3684dd7" width="400" alt="화상 강의"> |

| 강의 찾기 (Lecture) | 강의 상세 (Lecture Detail) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/09f1283c-c809-4ac4-85f7-441539510355" width="400" alt="강의찾기"> | <img src="https://github.com/user-attachments/assets/bb2823df-ff9b-4cba-87a4-f69230512fd3" width="400" alt="강의 상세"> |

| 결제 모달 (Toss Payments) | 관리자 (Admin) |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/d9f1b53c-e4b6-429e-bed0-8a04bf3cbad6" width="400" alt="결제 모달"> | <img src="https://github.com/user-attachments/assets/b83b17f8-7863-4473-88e1-09727131ac4b" width="400" alt="관리자"> |

| 마이 페이지 (My Page) |
| :---: |
| <img src="https://github.com/user-attachments/assets/66a84bf5-0a9b-4a19-b113-278effec17b7" width="800" alt="마이페이지"> 


<br>

## 7. 🚀 트러블 슈팅 (Trouble Shooting)

### ⚡️ 실시간 채팅(SSE) 미표시 문제 
WebRTC 강의실 내에서 채팅 전송은 되으나 화면에 표시되지 않는 오류 해결.

### ⚠️ 문제 발생 (Issue)

현상: 채팅 전송 성공 로그는 뜨지만, Mentor/Mentee 화면에 말풍선이 렌더링되지 않음.

원인: 백엔드(MyBatis ResultMap)에서 조회한 데이터를 DTO 객체가 아닌 **단순 문자열(text)**로 전송했으나, 프론트엔드는 JSON(DTO) 파싱을 시도하여 에러 발생.

### 🛠 해결 전략 (Solution)

Backend: 응답 데이터를 단순 문자열에서 MessageDTO 객체로 감싸서 전송하도록 수정.

Frontend: 메시지 핸들러 로직을 DTO 구조에 맞춰 통일.

### ✅ 결과 및 배운점 (Result)

모든 페이지에서 실시간 채팅이 정상 표시되며, 정렬 및 부가 기능 정상 동작.
