# 🍏 AI 기반 레시피 추천 웹사이트, Fridget
<img width="436" alt="Fridget Logo" src="https://github.com/user-attachments/assets/90350ef7-7f6f-41b3-8485-4d9d2a08c673" />
<br><br>

🔎 프론트엔드 코드는 [이 레포지토리](https://github.com/sinaetown/FridgetFrontend.git)를 참고해주세요.

---

## 🎥 Demo

- **Demo Video**: https://youtu.be/FFFVZ70Mt_E  
- **Sketch Video**: https://www.youtube.com/watch?v=RkE8c7gXehM

---

## ✨ Award

![8CFC0704-76D9-42F0-88CD-0B9FC7854B8A](https://github.com/user-attachments/assets/c4c4763f-c92c-4a20-ac42-ddd5a54639b1)
---

## 📌 Project Introduction
냉장고 속 재료만으로도 맛있는 요리를 찾을 수 있다면?
<br> Fridget은 OpenAI API를 활용하여 사용자가 가진 재료를 바탕으로 최적의 레시피를 추천해주는 AI 기반 웹사이트입니다.
<br>"오늘 뭐 먹지?" 고민하지 말고, AI가 대신 찾아주는 레시피를 활용하세요!

🚀 주요 기능
<p> 1️⃣ 스마트 레시피 검색: AI가 웹을 검색하여 사용 가능한 재료에 맞는 레시피를 찾아줍니다.
<p> 2️⃣ 개인 맞춤 추천: Nearest Neighbor 알고리즘을 활용하여 사용자의 식습관과 취향을 분석하고 반영합니다.
<p> 3️⃣ 선호도 기반 추천 랭킹: 사용자의 선호도를 고려하여, 알맞은 레시피를 우선적으로 추천하여 최적의 선택을 제공합니다.

## 🫡 Members
|-|Name|Role|
|--|------|---|
|💡|Samuel Han 한석현|Frontend|
|💎|Hojun Kwak 곽호준|Frontend|
|🕯️|Sinae Hong 홍신애|Backend|
|⚡️|Hanseung Choi 최한승|AI/ML|

## 🛠 Tech Stack

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Chakra UI](https://img.shields.io/badge/Chakra%20UI-319795?style=for-the-badge&logo=chakraui&logoColor=white)
![Material UI](https://img.shields.io/badge/Material%20UI-0081CB?style=for-the-badge&logo=mui&logoColor=white)

### Backend
![Java 11](https://img.shields.io/badge/java%2011-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Java Spring](https://img.shields.io/badge/Java%20Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![JSON Web Tokens](https://img.shields.io/badge/JSON%20Web%20Tokens-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

### AI/ML
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
---

## 🏛️ Design Architecture

![Fridget Architecture](https://github.com/user-attachments/assets/d9fd87f8-98a6-42b9-bb42-a1aaf5999612)

---

## 🚀 Server Execution Guide
**1. Redis 실행**
```bash
brew services start redis
```

**2. Flask 서버 실행 방법**

(1)
```bash
cd FridgetServer 
source venv/bin/activate
cd flask
```

<details> <summary> (2) Flask 서버 실행 전 필수 Dependencies 설치</summary><br>
  
```bash
pip install flask
pip install openai
pip install spacy
pip install scikit-learn
python -m spacy download en_core_web_md
```

</details>

(3) generate_recipes_flask.py 파일에서 OPENAI_API_KEY 설정
```bash
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxx
```

(4) Flask 서버 실행

```bash
python -m flask --app generate_recipes_flask run --host=0.0.0.0 --port=5001
```

**3. Spring Boot 서버 실행**
```bash
cd FridgetServer/
./gradlew build
java -jar build/libs/fridgeproject-0.0.1-SNAPSHOT.jar
```
