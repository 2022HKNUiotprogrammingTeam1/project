# **22.05.17. 1차 발표**

# **IoT 프로그래밍 프로젝트 계획 발표**

## **두더지 타일**

*   **2017250043 정유성**
*   **2016415024 이지환**
*   **2017250044 정재현**

<br/>

**목차**

1. 기존 프로젝트 조사 내용

2. 계획한 프로젝트

3. 기존 게임과의 차이, 차별성

4. 참고문헌

<br/>

### **1. 기존 프로젝트 조사 내용**

1. snake 게임
8x8 dot matirx에서 snake가 자신의 꼬리와 벽에 부딪히지 않고 먹이를 찾아 이동하며 점수를 획득하는 게임


2. 가위바위보 및 베팅 게임
배팅금액을 설정한 후 가위바위보 게임을 진행
가위바위보를 승리할 경우 배팅금액을 획득하고
가위바위보를 패배할 경우 배팅금액을 회수당하는 시스템
이후 모인 금액을 현금으로 전환하는 내용의 게임

<br/>

### **2. 계획한 프로젝트**

두더지 타일 ( 두더지 게임 + 피아노 타일 )

![Pic](./pic/molegame.png)
![Pic2](./pic/pianogame.png)


두더지 타일 ( 두더지 게임 + 피아노 타일 )

![Pic3](./pic/targetsystem.png)

*   dot matrix를 이용해 지속적으로 깜빡이는 불빛에 맞춰 해당
   위치에 상응하는 Swtich를 눌러 진행하는 방식

*   8x8 dot matrix중 최외각을 제외한 6x6크기의 matrix에서
   두더지 한마리의 크기를 2x2크기로 하는 3x3 필드

*   CLCD에 (진행도 + 점수) or (스코어 + 맞춘 개수) 등 게임에 대한 전반적인 내용 출력 예정

*   C언어 또는 C++언어 사용 예정

<br/>

### **3. 기존 게임과의 차이·차별성**

**두더지 게임 측면** : 두더지를 잡을수록 두더지가 생성되고 숨는 속도가 점점 빨라짐

**피아노 타일 게임 측면** : 두더지의 색상에 따라 점수가 두배가 되거나 마이너스 되는 효과 구현

<br/>

### **4. 참고문헌**

1. snake 게임 출처
https://github.com/jinwoo1225/SnakeGameWithSmart4412

2. 가위바위보 베팅게임 출처
https://syki66.github.io/blog/2020/06/15/H-smart4412TKU.html

3. 두더지 게임 사진
https://www.urbanbrush.net/downloads/%EB%91%90%EB%8D%94%EC%A7%80%EA%B2%8C%EC%9E%84-%EC%9D%BC%EB%9F%AC%EC%8A%A4%ED%8A%B8-ai-%EB%AC%B4%EB%A3%8C%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C-free-mole-game-vector/

4. 피아노 타일 게임 사진
https://webisfree.com/2016-01-25/[%EB%AA%A8%EB%B0%94%EC%9D%BC%EA%B2%8C%EC%9E%84]-%ED%94%BC%EC%95%84%EB%85%B8-%ED%83%80%EC%9D%BC2-%EA%B2%8C%EC%9E%84%EC%86%8C%EA%B0%9C-%EB%B0%8F-%EC%A0%84%EB%9E%B5

5. H-Smart4412TKU FPGA Board 사진
https://slidesplayer.org/slide/14109337/

**22.05.17 발표자 정유성**
