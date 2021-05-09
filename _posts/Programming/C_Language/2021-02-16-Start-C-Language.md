---
date: 2021-02-16
title: "[C Language] Introduction"
categories:
 - C_Language
tags:
 - [C, Programming]
comments: true
toc: true
toc_label: "Contents"
toc_sticky: true
---

안녕하세요! 🙋‍♂️ Code S 입니다! <br>
본 포스팅에서는 C언어가 무엇인지에 대해 알아보고, <br>
어떻게 C언어를 시작할 수 있는지에 대한 방법을 알려드립니다!
{:  .notice--success}

## 0x01. What is C Programming Language?

> 컴퓨터랑 대화를 할 수 있다고?! 😲🤩

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("hello world!\n");
	return 0;
}
```

가장 기본적인 프로그래밍 언어인 `C Programming Language`(a.k.a `C언어`)는 1972년 미국의 벨 연구소(Bell Labs)에서 `데니스 리치(Dennis M. Ritchie)`가 개발한 프로그래밍 언어입니다.

<p align="center"><img src="https://drive.google.com/uc?id=191J8_waHqwMsfu2N3m7fhRSyfU6uvNFY" alt="Dennis_Ritchie" width="300px" height="450px"></p>

처음에 `C언어`는 `UNIX` 라는 운영체제(Operating System)와 호환되는 다양한 프로그램을 개발하기 위해 사용되었습니다.  

그리고 `C언어`를 토대로 다양한 프로그래밍 언어(예를 들어 `C++`, `Java` 등등)가 발전하면서 다양한 프로그램들이 만들어지게됩니다.

## 0x02. History of C Programming Language

`C언어`라는 정말 좋은 언어가 탄생하기 전에도 다른 프로그래밍 언어가 존재하고 있었습니다.  

대표적으로 `포트란(Fortran)`, `코볼(COBOL)`이라는 언어가 존재했지만, 일반적으로 사용하기에는 매우 어려운 상황이었습니다.  

그러다가 1958년에 `ALGOL(Algorithmic Language)`라고 하는 언어가 등장을 하게 됩니다. 이 언어는 알고리즘의 연구개발, 수치 계산과 논리 연산에 이용하기 위한 목적으로 만들어졌으며 알골(Algol)계 컴퓨터에서 동작을 하였습니다.  

1960년에는 `ALGOL 60`이 등장했고, 이 언어로부터 `C언어`의 역사가 시작된다고 보면 됩니다.  

이 `ALGOL 60`이라는 언어에서 `CPL(Combined Programming Language)`이라는 언어가 탄생을 했고, 또 다시 1967년에 `BCPL(Basic CPL)`이라는 언어를 개발했습니다. 그리고 이 언어가 미국으로 가더니 `켄 톰슨(Ken Thompson)`이라는 벨 연구소의 한 프로그래머에 의해 `B언어 (B Language)`로 탄생하게 됩니다!  
(아이고 복잡해라...😵)  

흠흠..  
그리고 드디어!! `B언어`를 거쳐서 `C언어`가 탄생하게 됩니다!!!! (짝짝짝!!!)😆  

<p align="center"><img src="https://drive.google.com/uc?id=1oNh45SKDvWUuaO0Dl_o9qI1IU_72TiXp" alt="Hand Clap"></p>

`C언어`의 대략적인 탄생 순서에 대해 살펴보면 다음과 같은 순서가 되겠습니다!

<p align="cneter"><img src="https://drive.google.com/uc?id=1yVm506BP0jshtrxqxHo_AQ71tp3mat7N" alt="History_of_C"></p>

## 0x03. C, The most powerful Programming Language in the world!

`C언어`는 이후에 등장한 다양한 프로그래밍 언어에 직간접적으로 많은 영향을 주었고 이로 인해 `C언어`를 알고 있으면 다른 언어도 알기 쉽다는 말이 생겨나게 됩니다. 즉, 프로그래밍 언어의 세계에서 공통어로서의 역할을 한다고 볼 수 있죠!  

그러면 `C언어`는 어디에 사용되는 것일까요? 바로 핵심적인 응용 프로그램에는 다 쓰이게 됩니다!  

1. `C언어`는 임베디드 시스템(Embedded System)에 자주 사용됩니다.
2. 시스템 애플리케이션을 개발하거나 운용체제 내의 응용 프로그램을 개발하는데 사용됩니다.
3. 현재 우리가 많이 사용하고 있는 웹 브라우저인 `구글 크롬(Google Chrome)`의 전신인 `Google's Chromium`은 `C언어`로 개발되었습니다.
4. 데이터베이스 구조 질의어인 `SQL` 중 가장 유명하고 많이 사용되는 `MySQL` 또한 `C언어`로 개발되었습니다.
5. 스티브 잡스가 설립한 `애플(Apple)` 회사에서 개발한 운영체제인 `MAC OS X`도 `C언어`를 기반으로 만들어졌습니다.
6. 기타 등등

이렇게 수 많은 애플리케이션, 수 많은 운영체제가 `C언어`를 통해 개발되었습니다. 결국 `C언어`는 `프로그래밍 언어의 어머니`라고 보아도 무방할 정도로 그 영향력이 어마어마 합니다!  

### 0x03 - 1. How C Programming Language Works?

그렇다면 이렇게 엄청난 프로그래밍 언어인 `C언어`는 어떻게 동작을 하는 것일까요?  

바로 `컴파일(Compile)`을 통해 `Object File`로 변환되어 컴퓨터가 프로그래머가 원하는 동작을 수행할 수 있게 되는 겁니다.  

이러한 `컴파일`을 수행하도록 도와주는 프로그램을 우리는 `컴파일러(Compiler)`라고 부릅니다.  

<p align="center"><img src="https://drive.google.com/uc?id=1H-GE2U6PUioVgtOQDdd3sL3VLnZuXU_6" alt="process_of_compile"></p>

위 그림에서 볼 수 있듯이 간단하게 `컴파일`이라는 것은 `컴파일러`에 의해 컴퓨터가 실제로 읽을 수 있는 말로 바꿔주는 과정을 뜻합니다.  

이렇게 해서 우리는 컴퓨터와 서로 소통을 할 수 있게 되는 것이죠! 😆😆😆

## 0x04. Let's start programming with C!

> 이제 직접 컴퓨터랑 대화를 해보자!

그러면 본격적으로! `C언어`를 이용하여 `프로그래밍(Programming)`을 시작해보겠습니다!  

먼저, 컴파일러를 준비해야 하는데... 엄청 다양한 컴파일러들이 존재합니다.  

예를 들어, `gcc/g++`, `Visual C/C++`, `Turbo C/C++`, `Eclipse CDT` 등등..  

많은 종류가 있지만, 본 포스팅에서는 `Visual C/C++`을 이용하는 방법을 알려드리도록 하겠습니다!

### 0x04 - 1. Using Visual Studio

`Visual Studio`는 `마이크로소프트(Microsoft)`에서 만들어졌으며, 프로그램 소스코드(Source Code)를 작성할 수 있는 `에디터(Editor)`와 작성한 소스코드를 프로그램으로 만들어주는 `컴파일러(Compiler)` 등이 묶여있는 `통합 개발 환경(IDE, Integrated Development Environment)` 소프트웨어 입니다.  

이 `IDE`에 포함된 `컴파일러`가 바로 `Visual C/C++`입니다!  

설치방법은 너무 간단하기 때문에 따로 설명하지는 않겠습니다. 😅  

설치를 완료하였다면!  
지금부터 `Visual Studio`를 사용하여 `C언어 프로그래밍`을 해보도록 하겠습니다! (본 포스팅에서는 `Visual Studio 2019`를 사용하여 설명합니다.)  

1️⃣ 설치된 `Visual Studio` 프로그램을 실행하고, `[새 프로젝트 만들기(N)]`를 선택합니다.

<p align="center"><img src="https://drive.google.com/uc?id=1P9eBxUQhJqDlcZM0CXMlEl4GSqQ1STIm" alt="visual_studio_2019_01" width="550px" height="450px"></p>

2️⃣ `[빈 프로젝트]` 중에서 `Windows용 C++를 사용하여 처음부터 시작합니다. 시작 파일을 제공하지 않습니다.`라는 내용이 담겨진 프로젝트를 선택해서 만들어줍니다.

<p align="center"><img src="https://drive.google.com/uc?id=1_xPfOK_y3VN-LwpBsk7eGe_gYVbtosEY" alt="visual_studio_2019_02" width="550px" height="450px"></p>

3️⃣ `[새 프로젝트 구성]`페이지가 나타나면, `프로젝트 이름`, 프로젝트를 저장할 `위치`를 입력하고, `솔루션`의 경우 `솔루션 및 프로젝트를 같은 디렉터리에 배치(D)`라는 문구를 체크한 뒤, `[만들기(C)]` 버튼을 클릭해서 프로젝트를 생성합니다!

<p align="center"><img src="https://drive.google.com/uc?id=1l1djHXAEp7mDZjKR6lmlTOFAvDXmM_P2" alt="visual_studio_2019_03" width="550px" height="450px"></p>

4️⃣ 아래 그림과 같이 프로젝트가 생성되면, 화면이 나타나게 되며 `[소스 파일]`에 마우스 오른쪽 클릭을 해서 소스 코드 파일을 추가해줍니다.

<p align="center"><img src="https://drive.google.com/uc?id=1HtloQvNxqZQtGCyELDkLiqxgNFeqKZ-M" alt="visual_studio_2019_04" width="600px" height="500px"></p>

5️⃣ `[새 항목 추가]`라는 창이 하나 뜨게 되면, `C++ 파일(.cpp)`를 선택하고 파일 이름의 형태는 `[파일 이름.c]`로 한 뒤, `[추가(A)]`를 클릭합니다!

<p align="center"><img src="https://drive.google.com/uc?id=15688036XiXzfDnIadAE0SS1JKoUYZ2hc" alt="visual_studio_2019_05" width="550px" height="450px"></p>

6️⃣ 소스 코드 파일이 새롭게 추가되고, 입력을 할 수 있게 에디터 화면에 표시가 됩니다. 그러면 아래 그림과 같이 다음의 예제 소스 코드를 입력해줍니다!

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("hello world!\n");
	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1oQ9U3I3pnUIZqAouGzddSQS7-RJ2iNUO" alt="visual_studio_2019_06" width="600px" height="500px"></p>

7️⃣ 소스 코드 입력을 모두 마쳤으면..!! 이제 `[Ctrl + F5]`를 눌러 `컴파일(Compile)`을 진행하고 생성된 `exe 파일`을 실행하게 되면 결과를 확인할 수 있습니다! 😆😁

<p align="center"><img src="https://drive.google.com/uc?id=1Oa-5Sz2n4YEW6HExPE56t0oR9olWGh2p" alt="visual_studio_2019_07" width="800px" height="700px"></p>

## 0x05. Conclusion

여기까지 따라오셔서 소스 코드가 잘 실행이 되는 화면을 보셨다면 축하드립니다!! (짝짝짝!) 👏

<p align="center"><img src="https://drive.google.com/uc?id=1z5moRSebMC4YTjYE1z616mrn-_sNGrlW" alt="Hand Clap_2" width="300px" height="300px"></p>

`C언어 프로그래밍`을 하기 위해 무조건 `Visual Studio`만 사용할 필요는 없습니다. 이외에 다른 `IDE` 프로그램이 많이 존재하고 있으니 (예를 들어 `Eclipse`, `Turbo` 등등) 자신에게 맞는 `IDE` 또는 `Editor`를 이용해서 소스 코드를 작성하시면 됩니다!

그러면 다음 포스팅부터는 본격적으로 `C언어`에 대해 배우도록 하겠습니다!  ω༼'͡•-͡•༽ω 

<p align="center"><img src="https://drive.google.com/uc?id=1FvZWACMJPtul93yOZ8zrpy-QxxAUbYB3" alt="see_you_next_time" width="300px" height="300px"></p>

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}