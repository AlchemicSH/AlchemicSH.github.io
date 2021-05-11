---
date: 2021-05-10
title: "[C Language] Basic Structure of C Programming Language"
categories:
 - C_Language
tags:
 - [C, Programming]
comments: true
toc: true
toc_label: "Contents"
toc_sticky: true
---

안녕하세요! 🙋‍♂️ Code S 입니다!  
본 포스팅에서는 C언어의 기본적인 구조에 대해 설명합니다!
{: .notice--warning}

```c
/*
	File name: helloworld.c
	Writter: Code S
	Contents: Output Test of the Plain Text("Hello World!")
*/

#include <stdio.h>   // preprocessor

// main function
int main(int argc, char* argv[]) {
	printf("Hello World!\n");    // Output function
	return 0;
}
```

👨‍💻 위 예제를 이용해서 본 포스팅을 진행하도록 하겠습니다.  

`C언어(C Programming Language)`는 위 예제와 같이 기본 구조가 `주석(Comment)`, `전처리기(Preprocessor)와 헤더 파일(Header File)`, `메인 함수(Main Function)`으로 구성되어 있습니다.  

하나씩 차근차근 알아보도록 하겠습니다! 🙋‍♂️

## 0x01. Preprocessor and Header File

> 전처리기? 헤더 파일? 이게 뭐지? 😵

### 0x01 - 1. What is Preprocessor?

흔히 대학교 전공 중, `컴퓨터 공학(Computer Engineering)`이나 `컴퓨터 과학(Computer Science)`에서 배우게 되는 `전처리기(Preprocessor)`는 입력되는 데이터를 처리하여 다른 프로그램에 대한 입력으로서 사용되는 출력물을 만들어내는 프로그램이라고 배우게 됩니다.  

간단히 말하자면, 다음 그림과 같이 당근 주스를 만드려고 하는데..  
당근이 손질되어 있지 않으면 만들 수 없으니까~ 우선 당근을 손질하고 손질된 당근으로 당근 주스를 만드는 과정에서 당근을 손질해주는 기계를 `전처리기`라고 볼 수 있는 겁니다! (그래서 식당에 있는 주방에 들어가보면 `전처리실`이라고 따로 식재료 손질하는 곳이 존재하기도 하죠! ㅎㅎ)  

<p align="cneter"><img src="https://drive.google.com/uc?id=1pXd8OnCbq1DcAREejXNNtUJqCJVeYoc5" alt="explain_preprocessor"></p>

`C 언어(C Language)`에서의 `전처리기(Preprocessing)`또한 같은 개념입니다.  

우선, `프로그래밍(Programming)`에서 `전처리기`는 `컴파일` 직전에 실행되는 컴파일러의 별도의 프로그램으로, 전처리기가 실행되면 각 소스 코드에서 `지시자(Directives)`를 찾게 됩니다.  

`지시자(Directives)`는 `C 언어`에서 `#` 을 이용해서 선언하게 됩니다.  

`#include`, `#define`, `#ifdef`, `#endif`, 기타 등등..  

이러한 여러가지 `전처리기` 중에서 `#include`에 대해서 우선 배워보도록 하겠습니다.

### 0x01 - 2. What is Header File?

`전처리기(Preprocessor)`를 배우고 이 `전처리기`를 사용하려면 `지시자(Directives)`를 선언해야한다는 것을 배웠습니다. 그리고 그 중에서 기본적으로 무!조!건! 알아야 하는 것이 바로..  
`#include` 입니다.

```c
#include <stdio.h>
```

위와 같은 코드를 보고 `C언어`에서는.. `헤더 파일(Header File) 중 표준 헤더 파일인 [stdio.h]를 선언했다`라고 이야기 합니다.  

그렇다면, `헤더 파일`은 무엇일까요?  

`헤더 파일(Header File)`은 확장자 중 `.h or .H`를 갖는 파일을 지칭하며, 이 중 `표준 헤더 파일(Standard Header File)`은 `표준 라이브러리 함수(Standard Library Function)`들의 동작을 따로 정의해 놓은 파일을 의미합니다.  (읭? 😵)  

무슨 말이냐?! 하면.. 우리가 C언어로 프로그래밍을 할 때, `printf()`, `scanf()`와 같은 것들을 입력하는 것을 보았을 것입니다. 이 포스팅 맨 위에 적혀있는 예제 코드에서도 `printf()`가 있죠?  

이것을 C언어에서는 `함수(Function)`이라고 부르고, 이러한 기본적인 함수(표준 라이브러리 함수)들이 정의되어있어서 우리가 쉽게 사용할 수 있도록 편리성을 제공하는 것이 바로 `헤더 파일(Header File)`입니다!  

헤더 파일을 선언할 때, `<stdio.h>`처럼 꺽쇠 기호(<>)를 이용하는 경우를 `시스템 헤더 파일(System Header File)`이라고 부르고, `"myheader.h"`처럼 큰따옴표("")를 이용하는 경우를 `사용자 정의 헤더 파일(User Defined Header File)`이라고 부릅니다.  

이 둘의 차이점은 사전에 시스템에서 제공하느냐 사용자가 필요에 의해서 개발하느냐에 따라 다릅니다.  

## 0x02. Function

> 함수(Function)란 무엇인가? 😱

### 0x02 - 1. What is Function? (Basic)

학교를 다닐 때, 한 번 쯤 이런 그림을 본 적이 있을 것입니다.

<p align="cneter"><img src="https://drive.google.com/uc?id=1_-OI1MyXmh0vA6xzOuOdh4cTVwCw1VxX" alt="function_example"></p>

이것이 바로 함수입니다!  

예를 들어 설명하자면,  
`나는 천재다!`라는 문장을 출력하고 싶을 때, 이를 직접 구현하려면 많은 코드를 작성을 해야해서 힘들기 때문에 (실제로 엄청 힘듭니다;; ^^;;) `함수(Function)`를 만들어서 쉽게 기능을 구현할 수 있도록 하는 것이죠.

그래서 문장을 출력하려면..  

```c
printf("나는 천재다!");
```

이렇게만 하면 아주 간단하게 `기능`을 사용할 수 있죠! ㅎㅎ  

### 0x02 - 2. main() function

함수가 무엇인지 대략적으로 살펴봤으니 이제 예제 코드에 있는 `main` 함수에 대해 알아보도록 하겠습니다.  

> main() 함수는 프로그램 실행 시 운영체제(OS; Operating System)에 의해서 맨 처음 호출되고 맨 나중에 종료되는 함수이다.

`main()` 함수는 프로그램이 실행될 때 가장 먼저 호출이 되는 함수입니다. 이 함수는 운영체제가 호출을 하며, C 프로그램의 경우 소스 파일을 컴파일하고 링크해서 만든 실행 파일(`.exe`)을 실행하면 운영체제가 실행 파일 내의 main() 함수를 가장 먼저 호출하기로 사전에 약속되어 있습니다.  

C언어로 작성된 프로그램은 무!조!건! main() 함수를 반드시 가지고 있습니다!  

main() 함수의 선언 형태는 다음과 같이 나타낼 수 있습니다.

<p align="cneter"><img src="https://drive.google.com/uc?id=1k6F33Nush6ii7o30MXNKpFxByAsUKWSN" alt="main_function_structure"></p>

위 그림을 보면 간단하게 이해가 될 것입니다.

그럼 하나 씩 살펴보도록 하겠습니다.

먼저, `int`는 `integer`의 줄임말로 `정수`를 뜻합니다. 네.. 맞습니다! 여러분이 초등학교, 중학교, 고등학교 때 배웠던 수학에서 말하는 그 `정수` 맞습니다!  

이해되셨죠? ㅎㅎ  

결국 예제 코드에 적혀 있는 메인 함수는 간단히 풀이해보면 여러 입력`(int argc, char* argv[])`을 받아서 `main() 함수`를 호출한 후에 출력은 `정수(int형)`로 하라는 의미입니다.  

다음은 함수의 기능을 기술한 main() 함수의 기본 구조를 나타낸 것입니다.  

```c
int main(int argc, char* argv[])
{    // 함수의 시작
	 // 함수가 어떤 기능을 할 것인지 기술하는 곳!
}    // 함수의 종료
```

위 코드와 같이 함수의 시작은 중괄호 열기 `{`로 시작하고 중괄호 닫기 `}`로 종료하게 됩니다. 이는 C언어 프로그래밍을 할 때 기본적인 약속이므로 꼭 기억하고 있어야 합니다!  

이 중괄호 사이에는 함수가 어떤 기능을 할 것인지 기술을 하게 됩니다.  

실제로 함수가 호출되었을 때 해야 하는 기능을 정의하는 영역이죠!  (이를 `함수의 기능 영역`이라고 부르도록 하겠습니다.)  

`헤더 파일`에 대해 잠깐 살펴보았을 때, `printf()` 라는 함수도 `메인 함수`와 똑같이 `stdio.h`라는 헤더파일에 정의되어 있어서 우리가 편리하게 가져다가 쓸 수 있는 것이랍니다.  

> 세미콜론(;)은 문장의 끝을 의미하는 마침표와도 같은 존재!

함수의 기능 영역에서 잘 살펴보면 세미콜론(;)이 보이는 것을 확인할 수 있습니다. 편지나 보고서와 같은 글을 쓸 때 여러분은 문장이 끝났다는 의미로 마침표(.)를 찍습니다. 이처럼 C언어에서 세미콜론은 연산을 수행하는 문장의 끝을 나타내는 마침표를 의미합니다.  

> return 은 반환과 종료의 의미를 갖는다!

함수의 기능 영역에서 `return` 의 의미는 두 가지 의미를 가지고 있는데, 하나는 `함수를 호출한 영역으로 값을 반환한다`는 의미이고, 다른 하나는 `지금 이 함수를 종료한다`는 의미입니다.  

<p align="cneter"><img src="https://drive.google.com/uc?id=14Re365_fPa1u8Tkhrt94C2WVPww2EylK" alt="return_explain"></p>

이렇게 간략하게 `main() 함수`에 대해 살펴보았습니다. 아직 이해는 잘 안되겠지만 지금은 C언어의 기본적인 구조를 파악하는 것이 우선이기 때문에 여기까지만 설명하도록 하겠습니다.  

## 0x03. Comment

> 주석(Comment)에 대해 알아보자!

예제 코드에 보면 다음과 같이 적혀있는 것을 확인할 수 있습니다.  

```c
/*
	File name: helloworld.c
	Writter: Code S
	Contents: Output Test of the Plain Text("Hello World!")
*/
```

이것이 바로 주석입니다!!!! ㅎㅎ  

`주석(Comment)`이란 프로그램의 내용을 설명하고 프로그래머가 작성하는 메모를 의미합니다. 한 줄 주석은 `//`로 시작을 하고, 여러 줄 주석은 `/*`로 시작하고 `*/`로 끝납니다.  

```c
// 한 줄 주석

/* 여러 줄 주석_01
여러 줄 주석_02
여러 줄 주석_03
*/
```

이러한 주석이 필요한 이유는 무엇일까요?  

바로 `협동(Teamwork)` 때문입니다. 여러분이 회사에 프로그래머로 취직을 하게 되면 다양한 사람들과 소스 코드를 공유하면서 작업을 하게 되는데, 이 때 아무런 설명도 없으면 신입 프로그래머는 이해를 하기 힘들겠죠? 그래서 코드에 직접 메모를 해서 이 부분이 무엇인지 설명을 하기 위해 주석을 사용하는 것입니다.  

앞으로 여러분이 프로그램 코드 작성을 할 때 `주석`을 잘 활용하면 다른 사람들과도 공유하고 피드백도 받을 수 있는 좋은 프로그램 코드를 작성할 수 있게 되는 것입니다! 😆  

> 주석 처리 시 주의 사항은?

주석을 사용할 때, 여러 줄 주석(`/* */`)은 중복해서 사용을 하면 오류가 발생하게 됩니다. 만약 중복해서 주석을 사용하고 싶다면 `//`을 사용해야 합니다.  

<p align="cneter"><img src="https://drive.google.com/uc?id=1cvdSvCFY9b_m89GNx3Ft3ryLYLbaF9E-" alt="return_explain"></p>

## 0x04. Conclusion

지금까지 C언어의 기본 구조에 대해 알아보았습니다. 여기까지 잘 따라오신 여러분에게 박수!!! (짝짝짝!)  

<p align="cneter"><img src="https://drive.google.com/uc?id=1HuZq8wIeYN6lNFY5wbcbYQ6QoGiVSKid" alt="Hand Clap"></p>

앞으로 C언어를 배우는 길에서 꼭 알아야하는 것이기 때문에 잘 기억할 수 있도록 공부하셔야 합니다!  

그럼 다음 포스팅으로 만날게요! ω༼’͡•-͡•༽ω 

<p align="cneter"><img src="https://drive.google.com/uc?id=15sTfKooSbxMkkdsMmdysoDKcJ_ORioGm" alt="Bye Bye"></p>

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}