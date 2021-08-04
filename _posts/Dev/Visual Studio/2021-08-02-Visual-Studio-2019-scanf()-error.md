---
date: 2021-08-02
title: "[Visual Studio 2019] scanf() 함수 사용 시, 컴파일 에러 일시적 해결법!"
categories:
 - Visual_Studio_2019
tags:
 - [VisualStudio, VisualStudio2019, Microsoft]
comments: true
toc: false
---

안녕하세요! 🙋‍♂️ Code S 입니다! <br>
Visual Studio 2019 를 이용해서 처음으로 프로그래밍을 연습하는데 (특히 C언어!) scanf() 함수가 컴파일 에러가 나서 빌드를 할 수가 없는 경우에는?! 🤷‍♂️
{:  .notice}

> scanf() 함수 사용하고 싶어용! 😂

본 포스팅은 `Visual Studio 2019`를 기준으로 합니다.  

처음 C언어를 공부하시는 분들은 `scanf()` 함수를 연습하고자 코드를 작성하고 컴파일을 하게 되면 다음과 같은 에러 메시지를 확인할 수 있습니다.  

<p align="center"><img src="https://drive.google.com/uc?id=1sjpPTFOlHsSfhlhR4EDNxMVeBmphuRGQ" alt="scanf()_error_01"></p>
<p align="center"><img src="https://drive.google.com/uc?id=1JKHHyz3bJfXdkulRRUe8nmyqKDpsalt0" alt="scanf()_error_02"></p>

아닛??!! C언어 입문책이나 문서를 살펴보면 scanf() 함수가 기본이라고 나와있는데???? 사용을 못한다곳???!!!!!!!!!! 😡🤬🤬🤬😡😡😡🤬😫  

그러나 사용을 하지 못하게 막아 놓은 이유가 다 있답니다!!  

그 이유는!!!!!!!!!!!!!!!!!!!!!!!!!! 보안에 취약하기 때문!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! (???)  
scanf() 함수는 워낙 옛날에 나타난 함수이고, 보안 취약점 중에서 BOF(Buffer OverFlow) 취약점에 너무나도 나약한 녀석(?)이라서..,,,;; 요즘은 되도록이면 사용하지 못하게 막고 있는 것이랍니다람쥐....!!!!!!  

하지만, 정말 초보자 분들은 scanf() 함수부터 차근차근 프로그래밍 공부를 하는 것이 가장(!) 좋은 방법이기에~ 이를 해결할 방법을 소개해 드리고자 합니다!  

1️⃣ 자신의 프로젝트 속성으로 이동을 합니다.  

<p align="center"><img src="https://drive.google.com/uc?id=16Kz-N0E24dUe3H69pMBQdxDMW7XTNO5T" alt="scanf()_error_03"></p>

2️⃣ [C/C++] -> [일반] 메뉴를 선택하고, 목록 中 [SDL 검사] 목록으로 이동하여 [아니요(/sdl-)]를 선택하고 확인을 눌러줍니다.  

<p align="center"><img src="https://drive.google.com/uc?id=1-tIqDJ7V0pHgMQY3xfjN9v-0AV8prp3Z" alt="scanf()_error_04"></p>

3️⃣ 그리고 다시 컴파일을 진행하고 빌드를 하게 되면 정상적으로 `scanf()` 함수를 사용할 수 있는 것을 확인할 수 있습니다! 😁  

<p align="center"><img src="https://drive.google.com/uc?id=1tWwZvqHZ8p46HqrVxTdBEAYwqVTT0Sch" alt="scanf()_error_05"></p>

이제 여러분은 다시 C언어 공부를 진행할 수 있게 되었습니다!!!!!!!!!!!!!!!! (짝짝짝!!!!!!!!!)

<p align="center"><img src="https://drive.google.com/uc?id=1tFQSR_7w4N0p3cNldjWmgv0O0OHtUCwU" alt="짝짝짝!"></p>

끝. (End.)

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}