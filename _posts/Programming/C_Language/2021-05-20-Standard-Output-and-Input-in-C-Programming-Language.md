---
date: 2021-05-20
title: "[C Language] 03. Standard Output in C Programming Language"
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
본 포스팅에서는 C 언어의 표준 출력에 대해 알아보도록 하겠습니다!
{:  .notice}

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("Hello World!");     // 출력 함수 (C 언어 표준 출력)
	return 0;
}
```

## 0x01. Standard Output

> 표준 출력에 대해 알아보자!

### 0x01 - 1. printf() Function

`printf()` 함수는 이전 포스팅 중 `C 언어의 기본 구조`편에서 한 번 보았을 것입니다. 이 함수는 큰따옴표(`""`)로 묶인 내용을 모니터에 출력해주는 역할을 수행합니다. 그래서 `"Hello World!"` 같은 내용도 출력할 수 있는 것이죠~ ㅎㅎ (이는 앞선 `C 언어 소개`편에서 실제 컴파일을 하여 실행하는 것까지 실습을 진행했었습니다. 😁)  

만약 다른 내용을 출력하고 싶으면 큰따옴표(`""`) 안의 내용을 바꿔주기만 하면 됩니다.  

이 함수는 C 언어에서는 `표준 출력 함수(Standard Output Function)`이므로, 앞서 배웠던 전처리기를 이용한 헤더 파일 선언 중 `stdio.h` 를 헤더 파일로 선언을 해야만 사용을 할 수가 있습니다. `stdio.h`의 `stdio`가 바로 `Standard Input and Output`의 줄임말이기 때문이죠!  

그럼 printf() 함수 실습을 해보도록 하겠습니다.

```
사용하는 IDE: Visual Studio 2019 (Windows 10)
```

```c
// 첫 번째 printf()

#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("Hello World!");
	
	return 0;
}
```

```c
// 두 번째 printf()

#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("Hello World!\n");
	
	return 0;
}
```

위와 같이 두 개의 `printf()` 실습 예제가 있습니다. 두 코드의 차이점이 무엇인지 확인했나요?  

그렇다면 두 코드를 모두 입력하고 실행해보도록 하겠습니다!  

<p align="center"><img src="https://drive.google.com/uc?id=19LmXyLLmhQEmhdRoihC5i46OGyMata0E" alt="printf() function_01"></p>

차이점이 바로 보이죠? 바로 `'\n'` 입니다! ㅎㅎ  

단지 `'\n'`를 추가했을 뿐인데, 출력 결과가 깔끔하게 나타나는 것을 확인할 수 있습니다.  

`'\n'`는 현재 커서를 한 줄 아래로 옮기는 역할을 합니다. 즉, 우리가 문서 작성할 때 다음 줄에 입력을 하기 위해 `Enter`키를 입력하는 것과 같은 역할을 하는 것이죠.  

다시 정리해보자면, `printf()` 함수가 큰따옴표(`""`) 안의 내용들을 차례대로 화면에 출력을 하다가 `'\n'`을 만나게 되면 바로 다음 줄로 바꿔서 출력을 하게 되는 것입니다.  

이렇게 특수한 역할을 수행하는 문자들을 우리는 `특수 문자(Escape Sequence)`라고 부릅니다.  

### 0x01 - 2. Escape Sequences in C Programming Language

> C 언어에서는 다양한 특수 문자를 사용할 수 있다!

C 언어에서 사용할 수 있는 `특수 문자(Escape Sequence)`는 다음 표와 같습니다.  

|특수 문자(Escape Sequence)||설명(Character represented)|
|:---:||:---:|
|&#92;a||경고음 발생 (Alert; Beep, Bell)|
|&#92;b||백스페이스 (Backspace)|
|&#92;f||폼 피드 (Form Feed)|
|&#92;n||개행 (New Line), 키보드의 `Enter` 키 효과!|
|&#92;r||캐리지 리턴 (Carriage Return)|
|&#92;t||수평 탭 (Horizontal Tab), 키보드의 `Tab` 키 효과!|
|&#92;v||수직 탭 (Vertical Tab)|
|&#92;&#92;||역슬래시 (Backslash)|
|&#92;'||작은따옴표 (Apostrophe or Single Quotation Mark)|
|&#92;"||큰따옴표 (Double Quotation Mark)|
|&#92;?||물음표 (Quesion Mark)|

이 특수문자는 다 외우지 않아도 괜찮습니다. 필요할 때마다 참고해서 사용하면 되기 때문이죠~ ㅎㅎ (외우고 있기 귀찮기도 하공.. 😅)  

예제를 통해 직접 확인해보도록 하겠습니다!  

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("Hello World! \n");
	printf("\t Hello! \n\t My name is Code S! \n");
	printf("역슬래시: \\ \n");
	printf("작은따옴표: \' \' \n");
	printf("큰따옴표: \" \" \n");
	printf("물음표: \? \n");

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1hS1rbvVKcCrtglVqQ8tgR2Z9-gvpKS-U" alt="printf_escape_sequence_result"></p>

위 예제코드를 입력해보면 위와 같은 결과를 확인할 수 있습니다! 꼭 실습을 통해 직접 경험해보는 것이 가장 중요합니다! 😉

### 0x01 - 3. Format Specifiers in C Programming Language

다음으로 살펴볼 것은 `서식 문자(Format Specifiers)`입니다. `printf() 함수`는 `Print Formatted`라고 해서 `print`에 `f`를 추가하여 이름을 지었으며, 그 만큼 `서식화된 문자(서식 문자)`에 따라 다양한 출력 형식을 가지게 됩니다.  

`서식 문자`란 출력 형태를 지정해 주는 문자를 뜻합니다. 예를 들어..  

```c
printf("%d", 1+2);
```

위와 같은 `printf()` 예제가 있다면, 이 뜻은 `출력 화면에 %d를 출력해주세요!`가 아니라, `뒤에 있는 1+2 의 결과값은 3 이라는 것을 10진수로 표현해서 출력해주세요!`라는 뜻입니다. 10진수는 영어로 `Decimal`이라고 하죠. 네. 바로 10진수 영어 표현의 맨 앞글자인 `D`를 따와서 만든 서식 문자입니닷! ㅎㅎ  

그렇다면 16진수, 8진수는 어떻게 표현할까요? 16진수는 영어로 `HeXadecimal`, 8진수는 `Octal`이니까.. 각각 알파벳 `x`, `o` 를 이용하여 서식 문자인 `%x`, `%o`가 됩니다! (간단하죠? 😆)  

이처럼 `printf() 함수`는 단순히 문자 또는 문자열을 출력해주는 역할만 하는 것이 아닙니다. 이렇게 숫자 계산 결과도 출력할 수 있고, 이를 다양한 표현 방식으로 출력할 수가 있습니다. 그럼 이 `서식 문자`를 어떻게 사용하는지 예제와 함께 차근차근 알아보도록 하겠습니다! 🙋‍♂️

|서식 문자(Format Specifiers)||출력 형태(Output Forms)|
|:---:||:---:|
|%d or %ld or %i or %li||10진수 정수 (a decimal integer)|
|%u||10진수 정수 중 양의 정수만 표현 (unsigned decimal integer)|
|%x||16진수 정수 (a hexadecimal integer)|
|%o||8진수 정수 (an octal integer)|
|%f and %lf||10진수 실수 (a floating point number for floats)|
|%e||e 표기법에 의한 실수 (a floating point number in scientific notation)|
|%E||E 표기법에 의한 실수 (a floating point number in scientific notation)|
|%g or %G||소수점 이하 자리 수에 따라 %f, %e 둘 중 하나 선택 (Similar as %f or %lf or %e or %E)|
|%c||하나의 문자 (a single character)|
|%s||문자열(문장) (a string)|
|%%||% 기호 출력 (the % symbol)|

> 다양한 숫자를 출력해보자!

먼저 예제 코드를 살펴보도록 하겠습니다!  

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("※ %%d, %%i 사용해보기! ※\n");
	printf("\n");
	printf("%d + %d = %d \n", 10, 20, 10 + 20);
	printf("%i + %i = %i \n", 30, 90, 30 + 90);
	printf("%d - %d = %d \n", 10, 20, 10 - 20);
	printf("%i - %i = %i \n", 30, 80, 30 - 80);

	printf("\n");

	printf("※ 16진수(%%x), 8진수(%%o) 사용해보기! ※\n");
	printf("\n");
	printf("10진수: %d, 16진수: %x, 8진수: %o \n", 25, 25, 25);
	printf("But, 16진수와 8진수는 음수 표현 불가! \n");
	printf("10진수: %d, 16진수: %x, 8진수: %o \n", -25, -25, -25);

	printf("\n");

	printf("※ %%f, %%lf 사용해보기! ※\n");
	printf("\n");
	printf("10진수 정수: %d \n", 0.5);
	printf("10진수 실수: %f \n", 0.5);
	printf("10진수 실수: %lf \n", 0.5);
	printf("기본적으로 소수점 6자리 까지만 표현: %f\n", 0.1234567);
	printf("기본적으로 소수점 6자리 까지만 표현: %f\n", 0.1234564);
	printf("기본적으로 소수점 6자리 까지만 표현: %lf\n", 0.1234567);
	printf("기본적으로 소수점 6자리 까지만 표현: %lf\n", 0.1234564);

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1rQFlBtTwLDX8HwbRa6FhO-oeWumtLgtY" alt="number_output_test_result"></p>

다음과 같이 예제 코드를 입력하고 컴파일한 뒤 실행해보면 다음과 같은 결과가 나타나는 것을 확인할 수 있습니다.  

먼저, `%d`, `%i`를 사용한 예제 코드를 확인해보도록 하겠습니다.

```c
printf("※ %%d, %%i 사용해보기! ※\n");
printf("\n");
printf("%d + %d = %d \n", 10, 20, 10 + 20);
printf("%i + %i = %i \n", 30, 90, 30 + 90);
printf("%d - %d = %d \n", 10, 20, 10 - 20);
printf("%i - %i = %i \n", 30, 80, 30 - 80);
```

<p align="center"><img src="https://drive.google.com/uc?id=1QHKbokPXIWoM01nBNW_doznI5OmIKIbU" alt="printf_explain_01"></p>

`%d`, `%i` 모두 `10진수 정수 (양의 정수와 음의 정수)`를 표현하는 것을 확인할 수 있습니다. 물론 보통 프로그래밍을 할 때 10진수 정수를 표현하려면 `%d`를 가장 많이 사용합니다.  

다음으로 `16진수(%x), 8진수(%o)`를 사용한 예제 코드를 확인해보도록 하겠습니다.

```c
printf("※ 16진수(%%x), 8진수(%%o) 사용해보기! ※\n");
printf("\n");
printf("10진수: %d, 16진수: %x, 8진수: %o \n", 25, 25, 25);
printf("But, 16진수와 8진수는 음수 표현 불가! \n");
printf("10진수: %d, 16진수: %x, 8진수: %o \n", -25, -25, -25);
```

10진수인 `25`를 각각 16진수와 8진수로 표현을 한 예제 코드입니다. 양의 정수의 경우에는 16진수, 8진수 모두 표현이 가능하지만, 음의 정수의 경우 16진수와 8진수로는 표현이 불가한 것을 확인할 수 있습니다.  

다음은 `%f`, `%lf`를 사용한 예제 코드를 확인해보도록 하겠습니다.

```c
printf("※ %%f, %%lf 사용해보기! ※\n");
printf("\n");
printf("10진수 정수: %d \n", 0.5);
printf("10진수 실수: %f \n", 0.5);
printf("10진수 실수: %lf \n", 0.5);
printf("기본적으로 소수점 6자리 까지만 표현: %f\n", 0.1234567);
printf("기본적으로 소수점 6자리 까지만 표현: %f\n", 0.1234564);
printf("기본적으로 소수점 6자리 까지만 표현: %lf\n", 0.1234567);
printf("기본적으로 소수점 6자리 까지만 표현: %lf\n", 0.1234564);
```

먼저, 3 ~ 5번 라인의 코드를 확인해보도록 하겠습니다.  
저는 이 예제 코드에서 실수인 `0.5`를 표현하는 것으로 코드를 작성을 했는데, 결과 화면을 보게되면 `%d` 서식 문자를 이용하여 실수를 표현하려고 하면 표현이 되지 않는 것을 확인할 수 있습니다. 그러므로 실수를 표현하려면 무조건 `%f`나 `%lf`를 사용하는 것이 맞습니다.  

다음으로 6 ~ 9번 라인의 코드를 확인해보도록 하겠습니다.  
위 결과화면과 같이 실수를 표현하는 서식 문자인 `%f`와 `%lf`는 기본적으로 소수점 6자리까지 표현을 하게 되며, 6자리를 넘기는 수를 표현하려고 하면 반올림 또는 반내림 현상이 발생해서 오차가 생기게 됩니다. 그래서 `0.1234567`을 표현하게 되면 `0.123457`로 표현되고, `0.1234564`를 표현하게 되면 `0.123456`으로 출력이 되는 것입니다.  

> 문자와 문자열을 출력해보자!

이번에는 문자와 문자열을 어떻게 출력하는 것인지 확인해보도록 하겠습니다.  
먼저 예제 코드를 살펴보도록 하겠습니다.  

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("%c %c %c %c %c %c \n", 'a', 'A', 'b', 'B', 'c', 'C');
	printf("\n");
	printf("%c %s %c. \n", 'A', "is the uppercase letter of the lowercase letter", 'a');
	printf("\n");
	printf("%s = %d %s \n", "3 * 5", 3 * 5, "입니당!");

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=14nc5vFOWyjfcL0xk-B7vYe2n3190xbL-" alt="character_and_string_test_result"></p>

예제 코드와 결과 화면은 위와 같습니다.  

<p align="center"><img src="https://drive.google.com/uc?id=12UAu25L_k4kipL70nP6pQgA3Y1xG4j-1" alt="printf_explain_02"></p>

코드를 잘 확인해보면 `%c`는 `문자(character)`, `%s`는 `문자열(string)`을 뜻합니다. 그리고 `printf() 함수`에서 표현을 하려면 문자는 작은따옴표(`''`), 문자열은 큰따옴표(`""`)를 사용하는 것을 알 수 있습니다.  

> 10진수 정수 (양의 정수)를 출력해보자! - %u

이미 앞에서 10진수 정수를 표현하는 서식 문자인 `%d`와 `%i`에 대해서 배웠죠? ㅎㅎ 이번에는 또 다른 10진수 정수를 표현하는 서식 문자인 `%u`에 대해 알아보도록 하겠습니다!  

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("%u \n", 4294967295);

	printf("\n");

	printf("%d \n", 2147483647);

	printf("\n");

	printf("%d \n", 2147483650);

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=19vVIc2v2jfTrcWNTOFkv43xUEsLNFzj5" alt="printf_explain_03"></p>

무슨 차이인지는 잘 모르겠죠? ㅎㅎ 이것은 좀 더 뒤에 배울 `자료형(Data Type)`에서 배우게 되는 내용이지만 간단히 알아보도록 하겠습니다.  

`%d`는 10진수 정수 범위인 `-2,147,483,648 ~ 2,147,483,647`을 표현할 수 있는 것이고, `%u`는 10진수 정수 범위 중 양의 정수 범위만 표현할 수 있지만 음의 정수 범위를 표현 못하는 대신에 양의 정수 범위를 두 배까지 표현할 수 있습니다.  

즉, `%u`는 10진수 정수 범위인 `0 ~ 4,294,967,295`을 표현할 수 있는 것이죠! 😆  

우선은 이 정도까지만 알아보도록 하겠습니다. 좀 더 자세한 내용은 나중에 `자료형(Data Type)`에 대해서 배울 때 알아보도록 하겠습니다!  

> 출력할 때 숫자 칸을 지정해서 나타나게 하는 방법은 없을까?

앞으로 프로그래밍을 하면서 다양한 숫자를 출력하게 되면 깔끔하게 보이기 위해 숫자들의 칸을 미리 지정해서 같은 칸에 나타나듯이 출력하고 싶은 경우가 생길 것입니다. 다음과 같이 말이죠.  

<p align="center"><img src="https://drive.google.com/uc?id=19V1HFtk3eRfUDrUSZf1TwHXUm28yY5ut" alt="printf_explain_04"></p>

C언어에서도 이와 같이 미리 칸을 지정해서 출력이 가능합니다! 이를 `데이터 필드(Data Field)`라고 이야기합니다. 서식 문자에 옵션을 하나 추가하면 이 데이터 필드의 폭을 조절을 할 수가 있습니다. 예제 코드를 보면서 알아보도록 하겠습니다!

```c
#include <stdio.h>

int main(int argc, char* argv[]) {
	printf("%05d, %05d, %05d \n", 999, 9999, 99999);

	printf("\n");

	printf("%-5d, %-5d, %-5d \n", 999, 9999, 99999);

	printf("\n");

	printf("%+5d, %+5d, %+5d \n", 999, 9999, 99999);
	printf("%+5d, %+5d, %+5d \n", 999, -9999, 99999);

	return 0;
}
```

<p align="center"><img src="https://drive.google.com/uc?id=1ndeM8uVmvAOcp3av_eqlpoMvB9qY9kCh" alt="printf_data_field_test_result"></p>

위와 같이 예제 코드와 결과 화면이 있습니다. 한 줄 한 줄 알아보도록 하겠습니다.  

먼저, 4번 라인을 살펴보겠습니다. `%05d`라고 제가 서식 문자를 사용한 것을 확인할 수 있습니다. 이는 `데이터 필드(Data Field)를 5칸을 미리 확보하고 오른쪽 정렬로 출력하며 남은 자리는 0으로 채운다`라는 뜻입니다. 그래서 결과 화면을 보면 남은 자리에 숫자 0을 채워넣는 것을 확인할 수 있죠~ ㅎㅎ  

그 다음, 8번 라인을 살펴보겠습니다. `%-5d`라고 적혀 있습니다. 무슨 뜻일까요? 이는 `데이터 필드(Data Field)를 5칸을 미리 확보하고 왼쪽 정렬해서 출력한다`라는 뜻입니다. 그래서 결과 화면을 보면 왼쪽으로 정렬되어 있는 것을 확인할 수 있습니다!  

마지막으로 12 ~ 13번 라인을 살펴보겠습니다. `%+5d` 라고 적혀있죠! 이는 `데이터 필드(Data Field)를 5칸을 미리 확보하고 오른쪽 정렬로 출력하며 양수의 경우 +, 음수의 경우 - 부호를 붙인다`라는 뜻입니다. 마찬가지로 결과 화면을 보게되면 양수는 `+`, 음수는 `-` 부호를 붙여서 출력되는 것을 확인할 수 있죠! 😁  

## 0x02. Conclusion

이번 포스팅에서는 C 언어를 본격적으로 공부하면서 앞으로 여러분들이 수도 없이 사용하게 될 `표준 출력 함수(Standard Output Function)`에 대해 배웠습니다! 열심히 공부하는 여러분들에게 박수!!! (짝짝짝!!!)  

<p align="center"><img src="https://drive.google.com/uc?id=1sr3Z3OPbwBO8EkeL_sUmrC94Zj8QNiUC" alt="clapping_01"></p>

다음 포스팅에서는 `표준 입력 함수(Standard Input Function)`에 대해 알아보도록 하겠습니다! ╰(*°▽°*)╯

<p align="center"><img src="https://drive.google.com/uc?id=1EMJDO8HS9GMba0oHCYzOQBB8zl4OktW-" alt="bye_bye_01"></p>

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}