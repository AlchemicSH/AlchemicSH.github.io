---
date: 2021-05-26
title: "[Visual Studio 2019] 프로세스 ~ 이(가) 종료되었습니다. 라는 문구 없애기"
categories:
 - Visual_Studio_2019
tags:
 - [VisualStudio, VisualStudio2019, Microsoft]
comments: true
toc: false
---

안녕하세요! 🙋‍♂️ Code S 입니다! <br>
Visual Studio 2019 를 처음 설치하고 프로그래밍을 처음 시작해보려고 하는데, 명령 프롬프트(cmd.exe) 창에 "프로세스 ~ 이(가) 종료되었습니다." 라는 문장이 출력되면?! 🤷‍♂️
{:  .notice}

> "프로세스 ~ 이(가) 종료되었습니다." 문구를 없애보자!

본 포스팅은 `Visual Studio 2019`를 기준으로 합니다.  

처음 프로그래밍을 시작하려고 예제 코드를 입력하고 컴파일하고 실행까지 딱! 했는데..???!!  
다음과 같은 화면을 본 적이 있을 것입니다.  

<p align="center"><img src="https://drive.google.com/uc?id=1QCasdhOUcz7VmF1bbhy62yZ1b1uiHGjN" alt="Visual_Studio_2019_Debugging_01"></p>

실행 화면 창(명령 프롬프트 창)에 `프로세스 ~ 이(가) 종료되었습니다.`라는 문장이 뜨는데.. 이게 불편하지 않으면 굳이 없애지 않아도 좋지만 이 문장은 기본적으로 특수 문자 중 `줄 바꿈('\n')`을 실행하고 문장이 나타납니다.  

따라서 처음에 프로그래밍 문법을 익히면서 실행을 시키고 다른 책이나 강의에 나타나는 결과 화면과 다르게 나타나게 되어 혼란이 올 수도 있습니다.  

그러므로 이 문장이 나타나지 않도록 하는 것이 처음에 프로그래밍 공부를 할 때는 가장 좋다고 볼 수 있습니다.  

한 번 이 문장을 없애보도록 하겠습니다! 🙇‍♂️  

1️⃣ 먼저 맨 위에 보기 중에서 `[도구(T)]` 를 누르고, `[옵션(O)]`을 선택합니다.  

<p align="center"><img src="https://drive.google.com/uc?id=11Ge2hwBp6lYgl86wkbP9zuD5EzuFxnZ4" alt="Visual_Studio_2019_CMD_Option_Step_01"></p>

2️⃣ 그 다음, 나타나는 창에서 `[디버깅]` -> `[일반]`을 선택하고 맨 밑으로 스크롤을 내린 뒤 `디버깅이 중지되면 자동으로 콘솔 닫기`를 체크합니다. 그리고 `[확인]`을 눌러 설정을 저장합니다! 끝!!!!!! (쉽죠?? ㅎㅎ 🤣)  

<p align="center"><img src="https://drive.google.com/uc?id=173UEB7d4--LYQyD9EScn2jS-zdQC-yZ7" alt="Visual_Studio_2019_CMD_Option_Step_02"></p>

설정이 모두 끝났습니다! 이제 다시 `[Ctrl] + [F5]`를 눌러서 실행을 해보면..??!!  

<p align="center"><img src="https://drive.google.com/uc?id=1WyxzmBHA77RXwpJAw9RJgLqCb-PJrtfQ" alt="Visual_Studio_2019_Debugging_02"></p>

문장이 사라진 것을 확인할 수 있습니다!!!

<p align="center"><img src="https://drive.google.com/uc?id=1e80CUVowsfbMQgekxnNuqplr7l1JprcU" alt="짝짝짝!"></p>

끝. (End.)

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}