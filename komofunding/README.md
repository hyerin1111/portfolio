#  **Komofunding**
> 사용자의 프로젝트를 홍보하고 후원을 받을 수 있는 **크라우드 펀딩 플랫폼**입니다.


##  **기간**
- **2024.11.04 ~ 2024.12.18**

## 👥 **인원**
- **8명**




##  **소개**
Komofunding은 **크라우드 펀딩 플랫폼**으로, 사용자가 프로젝트를 등록하고 다른 사용자로부터 후원을 받을 수 있습니다.

---

## 🖥️ **홈 화면**
- **Framer motion**을 활용하여 다양한 애니메이션을 적용하고, **동적인 사용자 경험**을 제공합니다.



https://github.com/user-attachments/assets/1e83c3c1-4bd5-4505-b20c-4bcaa7a3ed4d




## 🖥️ **회원가입**


![회원가입 짧은 (1)](https://github.com/user-attachments/assets/3618d406-d71f-48a3-b3ba-868a8062c525)


![로그인](https://github.com/user-attachments/assets/1ff454e6-6fb9-41fa-b180-15f06b022293)



## 🖥️ **메인화면**
홈 화면에서는 운영자가 승인한 모든 프로젝트를 볼 수 있습니다.
특히, 후원 진행률(progressRate)이 높은 인기 프로젝트를 상단에 배치하여 쉽게 확인할 수 있도록 했습니다.
현재 프론트엔드에서 데이터를 받아 필터링하여 표시하는 방식으로 구현되어 있습니다.

🛠 프론트에서 처리하는 방식
1. /projects API를 호출하여 전체 프로젝트 데이터를 가져옵니다.
2. 현재 경로(pathname)를 확인하여 fundingStatus 값을 설정합니다.
  (예를 들어, /active이면 fundingStatus = "ONGOING"으로 설정, /upcoming이면 fundingStatus = "UPCOMING"으로 설정)
3. 프론트에서 fundingStatus에 따라 데이터를 필터링하여 화면에 렌더링합니다.
  (진행 중인 프로젝트만 보여주거나, 진행 예정 프로젝트만 보여주는 방식)


**Home: 운영자의 승인을 받은 모든 프로젝트**
"이 플랫폼에서는 다양한 크라우드 펀딩 프로젝트를 한눈에 확인할 수 있습니다.
React와 Zustand를 활용해 API 데이터를 가져와 필요한 정보만 필터링해서 화면에 보여주는 방식으로 구현했습니다

https://github.com/user-attachments/assets/feec46fb-058b-4306-8148-54efbd688d10

Upcoming : 아직 후원이 시작되지 않은 프로젝트  

https://github.com/user-attachments/assets/83b19248-2770-45f5-a0b6-ead9e94e3b54

Active : 현재 후원이 진행 중인 프로젝트

https://github.com/user-attachments/assets/f74db6bc-5bb8-4098-bf0e-2d67c5d8fb46



## 🖥️ **문의하기**

![문의하기](https://github.com/user-attachments/assets/431fda36-3949-4e89-97c9-b1e9d88d6d32)


## 🖥️ **결제**

https://github.com/user-attachments/assets/fc4cefc4-d73d-4cc8-99ce-07f033af3a2a

