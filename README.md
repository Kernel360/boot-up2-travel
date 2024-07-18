# Kernel360 Boot-up 프로젝트

### 🔲 [기획안 WIKI](https://www.notion.so/328f33a6d15948ecb81306de2372283b?v=2b3fd3e8647740aa8d0e4566ea804ca4&pvs=4) 링크

- **부트업의 목적**
    - **협업**에 대한 이해를 강화하고, **현실적 협업**에 대해 경험하는 것을 목표로 한다.
    - 구현보다는 **기능 설계와 문서화에 집중**하며 하나의 프로젝트를 만들 때 어떤 과정으로 어떻게 협업을 해야 하는지 배운다.
- **팀 구성**
    - 1~2일차 팀원
        
        KBE2_이선우, KBE2_이재윤, KBE2_김영래, KBE2_김민규
        
    - 3~4일차 팀원
        
        KBE2_박수형, KBE2_김택준, KBE2_김민규
        

---

# 🌈 테마별  종합 여행 플래너🧳

저희는 각 트렌드별 테마 키워드를 도출하고, 이를 활용한 인기 여행 장소를 추천합니다.

# ◾ 사용자 정의

1. **`Who?` *누가 사용하는가?***
    
    > **연인 또는 친구와 국내 여행을 가려하는 계획을 
    세울 여유가 없는 바쁜 20~30대 `사회 초년생`**<br/>
<image width="300px" src="https://github.com/user-attachments/assets/962fe485-fa7b-4951-b207-4c817003a721"/><br>
- `특징 0` 여행 계획을 세울 때 의견 취합에 어려움을 겪는다.<br/>
- `특징 1` 여행 계획을 세웠지만 잘 세운 것인지 확신이 없다.<br/>
- `특징 2`. **예산 한계**가 정해져 있다. (최대 허용 금액)<br/>
- `특징 3`. **예산 분배의 중요도가 서로 다르다**.
    
1. **`What?` 어떤 기능을 제공하나요?** 
   ### 1. 💁 최신 트렌드에 맞는 테마 별로 여행 장소를 추천해줍니다.
   ### 2. 📑 희망하는 여행 장소들을 플래너로 저장 및 관리합니다.
    <image width="" src="https://github.com/user-attachments/assets/26449a40-b173-4eeb-b428-b8d0f7e76e59"/>

# ◾ 저희는 이렇게 일했어요

- `figjam`을 활용한 서비스 흐름 설계
    
    https://www.figma.com/board/Te8t6jnDypR4RvjWsWz1o1/플로우차트?node-id=0-1&t=0yVVHZzur8uxmabH-0
    
- `Excalidraw`로 화면을 그리고 목표 기능을 도출 
   
   저의 팀이 진행한 MVP 기능 설계도 작업 화면 입니다.
   ![ttt](https://github.com/user-attachments/assets/4d4ec45a-bb7d-4528-8ea4-495b11ab2a50)
   https://excalidraw.com/#json=OW_9SGp7rQIzz9bks0Bmv,TlxCTFOx2dl--IXema-fhg

## ◾ ER 다이어그램
![TripDiary](https://github.com/user-attachments/assets/3c9f6ad6-ba08-4662-b962-4552da6de81d)
- https://www.erdcloud.com/d/zDM73NeDjkrGvurS3

## ◾ 아키텍쳐
![image](https://github.com/user-attachments/assets/5e05d849-6b4b-4f6c-a7f4-f21b51edb3ff)

### 프론트엔드
- React Native

### 백엔드

- Java 17
- Spring Boot
- Spring Batch

### DB
- MySQL

### 인프라
- AWS Cloud

### 사용하는 외부 API
- SK open API
- Social Login APi


## ◾ 기능 명세

### 사용자
<img width="818" alt="스크린샷 2024-07-18 오후 2 31 17" src="https://github.com/user-attachments/assets/874dafa4-023a-4802-a92a-8f7a87f7f8e6">

### 데이터
```JSON
{
  "status": {
    "code": "00",
    "message": "success",
    "totalCount": 1
  },
  "contents": {
    "stat": [
      {
        "ypId": "2814016",
        "ypName": "중문수두리보말칼국수",
        "category": "한식",
        "lat": 33.251545,
        "lng": 126.425064,
        "count": 1248,
        "distance": 6.465606214994677
      }
      //...
    ],
  }
}
```
<img width="833" alt="스크린샷 2024-07-18 오후 2 31 35" src="https://github.com/user-attachments/assets/e2d40b64-9704-4cfd-a9a1-3a886a5b9c79">

### 플래너
<img width="1041" alt="스크린샷 2024-07-18 오후 2 32 08" src="https://github.com/user-attachments/assets/c2d3a724-cec1-4fb8-8844-8f3501888820">
<image width="" src="https://github.com/user-attachments/assets/ab17322d-6e2d-4f07-9e26-a6f676b2f005"/>
<br/>
<image width="" src="https://github.com/user-attachments/assets/fcd87e57-2f56-4d26-94f4-f17dcd779995"/>
    
### 관리자
<img width="844" alt="스크린샷 2024-07-18 오후 2 32 22" src="https://github.com/user-attachments/assets/1278e9e3-860c-430a-aac8-930365287ff9">

---
## ◾ 고민했던점
1. 논란이 있을 수 있는 추상적인 테마에 대한 고민 ex) 인스타 명소, 대전최고맛집
  -> 테마를 추가할 때, 너무 추상적인 이름을 사용 할 경우 카테고리와 매칭에 어렵고 사용자들이 테마를 기준으로 장소를 검색할 때 혼란스러울 수 있음.
![image](https://github.com/user-attachments/assets/200e9075-013b-4c17-8e7b-3d63858ec8ea)
<br>
<br>
2. 테마, 카테고리, 장소 테이블 설계에 대한 고민

> 테마와 카테고리는 다대다 관계, 카테고리와 장소 또한 다대다 관계

> 다대다 관계를 표현하기 위해 테마-카테고리, 카테고리-장소 연결 테이블 추가

> 테마의 경우 사용자들에게 직접 표시되는 부분이기때문에 관리자가 직접 추가함

![image](https://github.com/user-attachments/assets/7bf52398-1a8d-4163-8e65-834f9bb07e66)

