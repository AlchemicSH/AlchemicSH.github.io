---
date: 2021-07-30
title: "[C Language] 04. Standard Input in C Programming Language"
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
본 포스팅에서는 C 언어의 표준 입력에 대해 알아보도록 하겠습니다!
{:  .notice}

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	int a, b;
	
	printf("a = ");        // Standard Output
	scanf("%d", &a);       // Standard Input
	
	printf("b = ");        // Standard Output
	scanf("%d",&b);        // Standard Input
	
	printf("%d + %d = %d\n", a, b, a + b);      // Standard Output
	
	return 0;
}
```

## 0x01. Standard Input

> 표준 입력에 대해 알아보자!

### 0x01 - 1. scanf() Function

이전 포스팅에서 `printf() 함수`에 대해 공부를 해보았습니다. `printf()`는 `출력!`을 위한 함수였죠? 반대로 `scanf() 함수`는 `입력!`을 하기 위한 함수입니닷! 😆  

우리가 키보드로 무엇인가를 입력받은 후에 (즉, 데이터를 입력받은 후에) 입력받은 데이터를 사용하려고 한다면 데이터를 먼저 저장을 해야겠죠? 이번 포스팅에서 배우게 될 `scanf()` 함수의 기본 기능 중 하나가 바로 데이터를 입력받아서 저장하는 것입니다.  

예를 하나 들어서, 다음과 같이 10진수 값(데이터)를 키보드로부터 하나 입력받아서 저장하려고 한다면 `scanf()` 함수를 다음과 같이 사용하면 됩니다.  

<p align="center"><img src="https://drive.google.com/uc?id=16KPzMpQDrQG6BMvwxVhffgijK1VvYQbQ" alt="scanf()_01"></p>

위의 예시에서 `%d`는 앞의 `표준 출력(Standard Output)`에서 배웠던 서식문자이며, 뒤에 나오는 `a`라는 변수에 데이터를 저장한다는 명령어를 보이고 있습니다.  

하지만, `printf()` 함수와 다른 점은 변수를 지정할 때, 변수 앞에 `&`라는 기호를 붙인다는 것을 알 수 있습니다.  

저 기호는 해당 변수가 할당된 메모리 주소를 의미하는 기호입니다. 즉, `a`라는 변수가 할당된 메모리의 주소에 입력값(데이터)을 저장하라는 뜻입니다.  

배달의 민족(!)인 우리가 음식(데이터)을 배달 주문하면, 우리집 주소로 음식이 배달되어 전달받는 것과 같은 의미입니다! 😁 (이 기호에 대한 내용은 후에 더욱 자세히 다룰 예정입니다! 😎)  

그럼 scanf() 함수 실습을 해보도록 하겠습니다.  

```
사용하는 IDE: Visual Studio 2019 (Windows 10)
```

우선 다음 예제 코드를 확인해보도록 하겠습니다.  

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	int age;
	
	printf("Input your age: ");
	scanf("%d", &age);
	
	printf("Your age is %d\n", age);
	
	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1GCc0vg4XwKy5S1AoxzR9T2PerU8EKCuQ" alt="scanf()_02"></p>

위 코드는 `scanf()` 함수를 실습하기 위한 아주 간단한 예제입니다. 나이를 입력하면 입력한 나이를 출력해주는 프로그램이죠.  

`age`라는 변수를 선언하고, 10진수 값(데이터)을 입력받아 `age` 변수에 저장한 뒤 출력하는 간단한 코드입니다.  

### 0x01 - 2. Format Specifiers in C Programming Language

> printf() 에서도 서식 문자가 있었는데 이게 그대로 적용되는 건가??!!

`scanf()` 함수 또한 `printf()` 함수와 같이 `서식 문자(Format Specifiers)`를 사용합니다.  

|서식 문자(Format Specifiers)||입력 형태(Input Forms)|
|:---:||:---:|
|%d or %ld||10진수 정수 (a decimal integer)|
|%u||10진수 정수 중 양의 정수만 표현 (unsigned decimal integer)|
|%x||16진수 정수 (a hexadecimal integer)|
|%o||8진수 정수 (an octal integer)|
|%f or %lf||10진수 실수 (a floating point number for floats)|
|%c||하나의 문자 (a single character)|
|%s||문자열(문장) (a string)|
|%e or %le||e 표기법에 의한 실수 (a floating point number in scientific notation)|

위 표에 적혀있는 서식 문자만 알고 있으면 거의 모든 코드를 작성할 때 불편함은 없을 것입니다. (만약 다른 서식 문자가 필요하다면 !!!<a href="https://www.google.com">구글GOD</a>!!! 에게 문의를 하면 됩니당! ㅎㅎ 🤣)  

예제 코드로 다양한 서식 문자들을 확인해보도록 하겠습니다.  

```c
#include <stdio.h>

int main(int agrc, char* argv[]) {
	int a, b, c;
	float d, e;
	double f, g;

	printf("10진수 정수 입력: ");
	scanf("%d", &a);

	printf("출력하기 => 10진수: %d, 16진수: %x, 8진수: %o \n", a, a, a);

	printf("\n");

	printf("16진수 정수 입력: ");
	scanf("%x", &b);

	printf("출력하기 => 10진수: %d, 16진수: %x, 8진수: %o \n", b, b, b);

	printf("\n");

	printf("8진수 정수 입력: ");
	scanf("%o", &c);

	printf("출력하기 => 10진수: %d, 16진수: %x, 8진수: %o \n", c, c, c);

	printf("\n");

	printf("float형 실수 두 개 입력: ");
	scanf("%f %e", &d, &e);

	printf("출력하기 => type_1 = %f, type_2 = %e \n", d, e);

	printf("\n");

	printf("double형 실수 두 개 입력: ");
	scanf("%lf %le", &f, &g);

	printf("출력하기 => type_1 = %lf, type_2 = %le \n", f, g);

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1qGtHxfdfWosHfDdFueVNNxT7Heh_SiZ8" alt="scanf()_03"></p>

위 예제를 통해 알 수 있듯이 `scanf()` 함수에서도 다양한 서식 문자를 사용할 수 있는 것을 확인할 수 있습니다! 😊  

## 0x02. Conclusion

이번 포스팅에서는 C 언어를 본격적으로 공부하면서 앞으로 여러분들이 수도 없이 사용하게 될 `표준 입력 함수(Standard Input Function)`에 대해 배웠습니다! 열심히 공부하는 여러분들에게 박수!!! (짝짝짝!!!)  

<p align="center"><img src="https://drive.google.com/uc?id=1wMdECl2epQkAKn7VmYlB0OcRTdWkh4CX" alt="clapping_01"></p>

다음 포스팅에서는 `변수(variable)`에 대해 알아보도록 하겠습니다! ╰(*°▽°*)╯  

<p align="center"><img src="https://drive.google.com/uc?id=1gm2wHCGtNm8CJTbpoF77oRdeRsgutonj" alt="bye_bye_01"></p>

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}