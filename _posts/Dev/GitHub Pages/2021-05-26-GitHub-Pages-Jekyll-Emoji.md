---
date: 2021-05-26
title: "[GitHub Pages] Jekyll 기반 블로그에서 Emoji 사용하기"
categories:
 - GitHub_Pages
tags:
 - [GitHub, Pages, Jekyll, Emoji]
comments: true
toc: false
---

안녕하세요! 🙋‍♂️ Code S 입니다! <br>
Jekyll 기반 블로그 (여기서는 Minimal Mistakes) 에서 이모지(Emoji)를 사용하려면??!!
{:  .notice}

> 이모지(Emoji)를 사용해보자!

처음 깃허브를 이용해서 블로그를 만들고 글을 몇 개 작성하면서 이모지를 사용해보았습니다. 저 같은 경우에는 이모지 사이트를 찾아가서 사용하고 싶은 이모지를 복사해서 글에 붙여넣어서 사용했지만, 일부 이모지가 나타나지 않는 현상을 발견했습니다.  

그래서 이것 저것 찾아보다가 Jekyll 플러그인 중 `jemoji`라는 것이 있는 것을 처음 알게 되었습니다! (진작 알았으면.. ㅠㅠ)  

우선, `minimal mistakes` 기반으로 구축된 블로그로 이야기를 하겠습니다.

방법은 너무나도 간단했습니다.  

블로그를 구축할 때 생성되는 파일 중 `Gemfile`과 `_config.yml` 두 개의 파일이 있습니다. 먼저, `Gemfile`에는..  

```
group :jekyll_plugins do
	gem "jemoji"
```

위와 같이 `jemoji`를 추가하면 됩니다.  

그리고 `_config.yml`에는..  

```
# Plugins (previously gems:)
plugins:
	- jemoji
```

위와 같이 `plugins:` 부분에 `- jemoji`라고 추가하면 됩니다! 😆😆😆😆😆  

---
[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}