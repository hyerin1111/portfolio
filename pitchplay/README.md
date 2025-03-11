#  **PitchPlay**
> PitchPlay는 축구 경기장 예약부터 경기 매칭, 팀 모집까지 지원하는 플랫폼입니다.
사용자는 간편하게 경기장을 예약하고, 개인 또는 팀 단위로 경기를 매칭할 수 있으며,
함께할 팀원들을 모집하여 더욱 원활한 경기 참여가 가능합니다.
PitchPlay는 직관적인 인터페이스와 편리한 시스템을 통해
축구 커뮤니티 활성화와 즐거운 경기 경험을 돕는 역할을 합니다.

##  **기간**
>2024.11.04 ~ 2024.12.18

## 👥 **인원**
>8명

**📌 Technologies & Tools (PitchPlay)**
Category	Technologies & Tools
OS	Windows, Mac OS
Programming Languages	Java, JavaScript
Frameworks	Spring Boot, React
Database	MariaDB
Libraries	JPA, Lombok, Styled-Components, Framer Motion, Axios
API	RESTful API (Spring Boot 기반)
Tools	GitHub, IntelliJ, HeidiSQL, Figma
Additional Technologies	LocalStorage, React Hooks (useState, useEffect)


## ✅ 주요 기여도

**📌 프론트엔드 개발**

React + Styled-Components를 활용한 UI 개발
Framer Motion을 활용한 애니메이션 및 동적 UI 구현 → 부드러운 인터랙션 제공
React 상태 관리 (useState, useEffect) 활용 → 경기 매칭 필터링 및 데이터 저장
매칭 필터 모달 개발 → 날짜, 성별, 팀 크기, 지역 등을 선택하여 맞춤형 매칭 가능
로컬 스토리지(LocalStorage) 활용 → 사용자 필터 설정을 저장하여 편의성 증가
백엔드 API 연동을 고려한 데이터 구조 설계 → RESTful API와 매끄러운 데이터 연결

**📌 백엔드 개발**

Spring Boot + JPA를 활용한 CRUD 기능 및 매칭 시스템 설계
소셜 매칭 서비스 개발 → 매칭 생성, 조회, 수정, 삭제 API 구현
예약 시스템과의 연동 → 경기 예약 정보와 매칭 데이터 간 관계 설정
DTO를 활용한 데이터 입출력 최적화

**📌 시스템 설계 & API 명세서 작성**

Figma를 활용한 서비스 와이어프레임 및 사용자 흐름 설계
RESTful API 명세서 작성 → 데이터 요청 및 응답 형식 정의하여 협업 효율성 증대
비즈니스 로직 정리 및 데이터베이스 모델링

---

📌 기능 상세 설명
1️⃣ 팀 매칭 (Team Matching)
사용자는 필터링(지역, 성별, 날짜)과 정렬 옵션(최신순 등)으로 원하는 매칭을 찾을 수 있음
useOutletContext()를 활용해 전역 필터링 상태 공유
axios를 활용하여 JSON 데이터 불러오고 useEffect로 상태 업데이트
🚀 관련 백엔드 API: GET /api/social-match (매칭 목록 조회)
2️⃣ 용병 모집 (Guest Player Recruitment)
사용자가 용병을 모집하는 게시글을 작성하고, 지원 가능
Quill을 활용한 WYSIWYG 에디터로 공고 작성
axios.get()을 활용해 경기장 정보, 예약 정보 등을 동기적으로 불러와 적용
지원 시 모달 팝업 및 알람 UI 적용
🚀 관련 백엔드 API: POST /api/social-match (매칭 생성)
3️⃣ 구장 예약 (Stadium Reservation)
사용자가 원하는 구장을 선택하고 예약 가능
Kakao Map API를 연동하여 위치 정보를 지도에 표시
navigator.clipboard.writeText()를 활용한 주소 복사 기능 제공
로그인 상태 확인 후 예약 가능하도록 설정
🚀 관련 백엔드 API: POST /api/reservation (예약 등록)
4️⃣ 소셜 매칭 (Social Match)
사용자가 직접 경기 매칭을 만들고, 참가자 관리 가능

백엔드 주요 기능:
✅ 매칭 생성 (POST /api/social-match)
✅ 매칭 조회 (GET /api/social-match/{matchNumber})
✅ 매칭 수정 (PUT /api/social-match/{matchId}) → 멤버 추가 가능
✅ 매칭 삭제 (DELETE /api/social-match/{matchId}) → 논리 삭제 적용

🔥 특징:

최대 인원 초과 시 자동 제한
경기 시작 시간 업데이트 가능
고유한 6자리 숫자 매칭 번호 생성

---

<br>

## 🖥️ **홈 화면**




https://github.com/user-attachments/assets/cf5eb3f0-642a-446f-8e07-f3a59433d3b7



---

## 🖥️ **메인 화면**

>PitchPlay의 홈 화면은 직관적인 UI와 반응형 디자인을 바탕으로 사용자 경험을 최적화하였습니다. 
주요 서비스(소셜 매칭, 팀 매칭, 경기장 예약)로 쉽게 이동할 수 있으며, 
헤더와 메뉴 드롭다운을 통해 다양한 기능을 편리하게 이용할 수 있습니다.

---

### 🔹 **구성 요소**
#### ✅ **메인 레이아웃**
- `Header`, `Footer`, `Outlet`을 포함한 페이지 구조 유지
- 일반 사용자와 관리자를 위한 헤더 분리 적용

#### ✅ **서비스 선택 섹션**
- 소셜 매칭, 팀 매칭, 경기장 예약 기능 제공
- 클릭 시 해당 서비스로 이동하는 인터랙션 적용

#### ✅ **헤더 - 주요 기능**
- 로그인/로그아웃 버튼 제공 (사용자 상태에 따라 변경)
- 검색 기능 모달 창 지원
- 관리자 페이지 접근 제한 설정 (일반 사용자는 접근 불가)

#### ✅ **메뉴 드롭다운 (사이드바)**
- 메뉴 버튼 클릭 시 `Framer Motion`을 활용한 애니메이션 효과 적용
- 소셜 매칭, 팀 매칭, 경기장 예약, 공지사항 등 주요 메뉴 제공
- 로그인 상태에 따라 **로그아웃 버튼 활성화**

---

## 📌 **홈 화면 기능 요약**

| **기능** | **설명** |
|----------|--------------------------------|
| **메인 레이아웃** | `Header`, `Footer`, `Outlet` 구조 유지 |
| **서비스 선택** | 소셜 매칭, 팀 매칭, 경기장 예약 선택 가능 |
| **헤더 메뉴** | 로그인, 검색, 관리자 페이지 접근 기능 포함 |
| **메뉴 드롭다운** | `Framer Motion`을 이용한 애니메이션 적용 |

---

PitchPlay의 홈 화면은 **사용자의 편의성과 직관적인 UI/UX**를 고려하여 설계되었으며, 
반응형 디자인을 적용하여 다양한 디바이스에서 최적의 경험을 제공합니다. 🚀⚽

