# uArm_Omok
## 프로젝트 개요
알파 오목이 서버에서 오목을 두면, 그 정보를 받아서 로봇팔이 바둑돌을 해당 위치에 두는 uArm 개발

## 프로젝트에 사용된 물품
- uArm Swift Pro
- C타입 케이블
- 아두이노 메가보드
- SuctionCup
- 바둑돌 등등

## 프로젝트 
우선, 프로젝트를 진행하기 위해서는 기본적으로 아두이노 스케치와 Xloader라는 프로그램이 필요합니다.
- [아두이노 스케치](https://www.arduino.cc/en/Main/Software)
- [Xloader 다운로드](http://xloader.russemotto.com/)  
설치가 되어있지 않다면 위 링크에 들어가서 설치 하시길 바랍니다.


1) Xloader를 활용하여, uArmSwiftPro_2ndUART.hex를 uArm에 업데이트 시켜줍니다.
2) 아두이노 스케치를 이용하여 Omok 코드를 열어줍니다.
3) 아래 코드의 값들을 각각 세팅해줍니다.
```c
int OmokNum = 0; //오목돌을 몇번째 두는가에 대한 정보
int useX = 104;//X초기값
int useY = -149; //Y초기값
int useDimensionX = 4; //X의 차원
int useDimensionY = 2; //Y의 차원
int use_length = 47; //사용하는 바둑집의 길이

int omok_demention = 9; //바둑판 크기 a*a이면 omok_demention = a
int omok_length = 25; //바둑판 착점의 한칸의 크기
int firstX = 131; //바둑판 최우측하단의 X좌표
int firstY = -95; //바둑판 최우측하단의 Y좌표
```
위 6개의 변수는 바둑돌의 집에 대한 변수이고, 아래 4개의 변수는 바둑판에 대한 변수입니다.

바둑판은 uArm을 기준으로 우측 최 하단 부분의 좌표가 초기 값이 됩니다.  
바둑알 집은 uArm 기준으로 좌측 최 하단 부분의 좌표가 초기값이 됩니다.

4) 세팅이 완료되었다면, 메가보드에 업로드시켜줍니다.
5) 메가보드와 uArm을 연결시켜주면 사용이 가능합니다.


ps) uArmStudio를 사용하기 위해서는, Xloader를 활용해 uArm을 Standard로 업데이트 시켜주어야합니다!
