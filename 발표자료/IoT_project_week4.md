# **22.06.07 IoT 프로그래밍 4차 중간 발표**

*   **2017250044 정재현**
*   **2017250043 정유성**
*   **2016415024 이지환**

**발표자 : 정재현**

<br/>

## 1. 구현한 코드들과 내용

+ **플레이어의 점수와 두더지의 점수를 CLCD에 표시**

+ **10번 스위치를 눌렀을 때 아이템 사용 가능. 두더지 10마리를 자동으로 잡아준다.**

+ **두더지는 한마리당 1점이다.**

+ **두더지를 놓쳤을 경우 두더지가 점수를 얻는다.**

+ **플레이어가 10점 단위로 점수를 얻었을 경우 다음 스테이지를 진행한다.**

<br/>

## 2. 게임의 각 단계를 적용

+ **스테이지 1단계에서는 두더지가 1마리씩,  스테이지 2단계에서는 두더지가 2마리씩, 스테이지 3단계에서는 두더지가 3마리씩 나온다.**


<br/>

## 3. 두더지 게임 1,2,3 단계 코드

[Mole_Stage.c](https://github.com/2022HKNUiotprogrammingTeam1/project/blob/main/%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C/Code/Mole_Stage.c)

<br/>

**Stage 1,2,3 영상**

https://www.youtube.com/watch?v=etlcd87EK2s

<br/>

## 4. 아이템과 점수 코드

[Mole_CLCD.c](https://github.com/2022HKNUiotprogrammingTeam1/project/blob/main/%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C/Code/Mole_CLCD.c)

<br/>

## 5. 아이템과 점수, 스테이지를 적용한 영상

https://www.youtube.com/shorts/duuKuOObT9s

<br/>

**코드**
[Mole_Game_main.c](https://github.com/2022HKNUiotprogrammingTeam1/project/blob/main/%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C/Code/Mole_Game_main.c)

<br/>

## 6. 마지막 점검 사항

+ **속도를 조절해 게임의 난이도를 조절**

+ **획득한 아이템의 개수를 led로 표시**

+ **플레이어와 두더지의 승,패**


<br/>

## 7. 참고 문헌



