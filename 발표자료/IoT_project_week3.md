# **22.05.24 IoT 프로그래밍 3차 중간 발표**

*   **2017250044 정재현**
*   **2017250043 정유성**
*   **2016415024 이지환**

<br/>

**목차**

1. 외부 입출력 장치 작동 확인

코드를 통해 타겟시스템의 외부 입출력 장치를 작동시키는법을 알고자
테스트를 진행하였음.

결과

리눅스 환경에서 C 코드 작성 -> 컴파일 -> 


2. 두더지 생성

![molerandom](https://user-images.githubusercontent.com/42956142/171040131-35691f1e-3d91-4ef9-97e8-e59a82b54963.gif)

DotMatrix에 두더지를 랜덤하게 생성하도록 하였다.

현재는 2초를 간격으로 한마리씩 나오도록 되어있다.

이후 간격을 좀더 다양하게 늘리고
한마리가 아닌, 여러마리가 나올수 있도록 수정해나갈 계획


3. Dot Matrix <-> tact sw 연동 확인

![tactsw](https://user-images.githubusercontent.com/42956142/171039957-e1ea9ae1-1c56-48c6-8567-4dffea4b4a04.gif)

tact sw와 Dot Matrix가 연동되도록 코드를 작성하였다.

1~9번 버튼을 누르면 Dot Matrix의 위치에 맞는 두더지가 잡히고
다음으로 넘어가게 된다.

12번 버튼을 누르면 종료하게 된다.

향후 10, 11번 버튼을 통해 아이템을 사용할수 있도록 할 예정.

4. 코드

```C
#include <asm/ioctls.h>
#include <fcntl.h>
#include <stdbool.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <sys/ioctl.h>
#include <sys/signal.h>
#include <sys/stat.h>
#include <sys/types.h>
#include <termios.h>
#include <time.h>
#include <unistd.h>

#define dot "/dev/dot"

unsigned char mole[9][8] = {
    // 도트 매트릭스 화면
    {0x00, 0x60, 0x60, 0x00, 0x00, 0x00, 0x00, 0x00}, //7번두더지
    {0x00, 0x18, 0x18, 0x00, 0x00, 0x00, 0x00, 0x00}, //8번두더지
    {0x00, 0x06, 0x06, 0x00, 0x00, 0x00, 0x00, 0x00}, //8번두더지
    {0x00, 0x00, 0x00, 0x60, 0x60, 0x00, 0x00, 0x00}, //4번두더지
    {0x00, 0x00, 0x00, 0x18, 0x18, 0x00, 0x00, 0x00}, //5번두더지
    {0x00, 0x00, 0x00, 0x06, 0x06, 0x00, 0x00, 0x00}, //6번두더지
    {0x00, 0x00, 0x00, 0x00, 0x00, 0x60, 0x60, 0x00}, //1번두더지
    {0x00, 0x00, 0x00, 0x00, 0x00, 0x18, 0x18, 0x00}, //2번두더지
    {0x00, 0x00, 0x00, 0x00, 0x00, 0x06, 0x06, 0x00}  //3번두더지
};

int main() {
    int dot_d, i, random;
    dot_d = open(dot, O_RDWR);
    if(dot_d < 0)
    {
        printf("오류 발생");
        exit(0);
    }
    
    for(i=0; i<9; i++)
    {
        random = rand()%9; //난수 생성
        write(dot_d, &mole[random], sizeof(mole));
        sleep(50000);
    }
    close(dot_d);

    return 0;
}
```
5. 참고 문헌
hello world 만들기
https://comonyo.tistory.com/5

Dot matrix 작동하기
https://comonyo.tistory.com/16

tact sw 작동하기
https://deepbugging.tistory.com/entry/HSMART-4412-%EC%97%90%EC%84%9C-Tact-Swich-%ED%99%9C%EC%9A%A9%ED%95%98%EA%B8%B0
