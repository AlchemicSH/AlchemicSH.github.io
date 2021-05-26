---
date: 2021-05-25
title: "[GitHub Pages] Code Block에 줄 번호(Line Number) 출력하기"
categories:
 - GitHub_Pages
tags:
 - [GitHub, Pages]
comments: true
toc: false
---

안녕하세요! 🙋‍♂️ Code S 입니다! <br>
깃허브(GitHub)로 웹호스팅(GitHub Pages)하고 있는데, 코드 블럭(Code Block)에 줄 번호(Line Number) 어떻게 출력할까요???
{:  .notice}

> 줄 번호를 내놔라! (Where is my Line Number in Code Block?)

`GitHub Pages`를 이용해서 웹호스팅을 이용하는 분들은 쉽게 웹 블로그 혹은 웹 페이지를 하나 간단하게 만들 수 있는 것을 확인할 수 있습니다. 매우 편리하고 사용하기도 쉽죠.  

그리고 `마크 다운(MarkDown)` 문서를 이용해서 글을 작성을 할 수 있죠! 여기서 문제가 발생합니다..  

만약 프로그래밍 관련 글을 작성하려고 코드 블럭(Code Block)을 사용했는데, 줄 번호(Line Number)를 같이 출력하고 싶지만, 처음에는 그 기능을 사용할 수 없어서 조금 불편함이 존재하죠.  

그래서 그 사용법을 알려드리고자 합니다. 매우 간단합니다! 😆  

웹 블로그를 목적으로 `깃허브 페이지(GitHub Pages)`를 이용한다면, `jekyll` 기반으로 만들어지기 때문에 `_config.yml`이라는 파일이 존재할 것입니다.  

이 파일을 열고, 맨 마지막 줄에 가서 다음 코드를 입력만 하면 끝입니다! (너무 간단하죠?? ㅎㅎ 🤣)  

```
markdown: kramdown
kramdown:
    highlighter: rouge
    syntax_highlighter_opts:
        block:
            line_numbers: true
```

그리고 `Push`를 한 다음 사이트에 접속해서 확인을 해보면 줄 번호(Line Number)가 코드 블럭(Code Block)에 뜨는 것을 확인할 수 있습니다! 👍😁😎



---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}