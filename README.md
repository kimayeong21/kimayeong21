# 👋 김아영 (Ayeong Kim)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6a11cb,100:2575fc&height=200&section=header&text=Ayeong%20Kim&fontSize=40&fontColor=ffffff"/>
</p>

---

### 🚀 About Me
AI 및 데이터 처리 기반 시스템 개발에 관심을 갖고 공부하고 있는 컴퓨터공학 전공자입니다.  
데이터 수집 → 처리 → 분석 → 시각화까지 이어지는 **전체 흐름을 직접 구현하는 개발자**를 목표로 합니다.

- 🎓 서원대학교 IT문화예술대학 컴퓨터공학과 졸업예정 (2027.02)  
- 🤖 융합 로보테크 AI 자율주행로봇 개발자 과정 2기 수료 예정 (2026.07)

---

### 📂 Projects

| 프로젝트 | 설명 | 기술 스택 |
|--------|------|----------|
| 🎬 Movie Recommendation System | 사용자 선호 기반 영화 추천 프로그램 (로그인, 관리자 기능 포함) | C |
| 🚌 Smart Schedule & Bus Management | 일정 및 버스 정보 통합 웹 서비스 (CRUD 구현) | Python, Flask, MySQL |
| 📊 Student Grade Management | 성적 관리 및 평균 계산 프로그램 | C |
| 💧 Smart Water Quality Monitoring | OpenCV 기반 물 색상 분석 + Arduino LED 제어 시스템 | Python, OpenCV, Arduino |

---

### 💧 Smart Water Quality Monitoring System

> OpenCV + 시리얼 통신 기반 실시간 수질 상태 분석 시스템

✔ 주요 기능  
- HSV 기반 색상 필터링을 통한 물 색상 감지  
- 픽셀 수 계산으로 상태 판단  
- Arduino RGB LED 제어  
- 상태 로그 자동 저장  

✔ 상태 분류 기준  
오염(갈색) → RED BLINK
녹조(초록) → BLUE BLINK
정상(파랑) → GREEN
감지 실패 → OFF


---

### ⚙️ 핵심 코드

```python
def detect_water_color(frame):
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)

    brown_mask = cv2.inRange(hsv, brown_low, brown_high)
    green_mask = cv2.inRange(hsv, green_low, green_high)
    blue_mask = cv2.inRange(hsv, blue_low, blue_high)

    b_pix = np.sum(brown_mask)
    g_pix = np.sum(green_mask)
    bl_pix = np.sum(blue_mask)

    if b_pix == max(b_pix, g_pix, bl_pix):
        return "오염 (갈색)"
    elif g_pix == max(b_pix, g_pix, bl_pix):
        return "녹조 (초록)"
    else:
        return "정상 (파랑)"

Languages

<p> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> <img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=C&logoColor=white"/> <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=C%2B%2B&logoColor=white"/> <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white"/> </p>

Frameworks & Tools

<p> <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=Flask&logoColor=white"/> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=OpenCV&logoColor=white"/> <img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=Arduino&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/> </p>
📊 GitHub Stats
<p align="center"> <img src="https://github-readme-stats.vercel.app/api?username=kimayeong21&show_icons=true&theme=radical"/> <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kimayeong21&layout=compact&theme=radical"/> </p>
📫 Contact
📧 Email: cngot0000@baver.com
💻 GitHub: https://github.com/kimayeong21
