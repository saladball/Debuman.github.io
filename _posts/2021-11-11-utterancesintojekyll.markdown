---
layout: post
title:  "jekyll 블로그에 utterances 연동하여 댓글기능 활성화"
date:   2021-11-11 14:52:36 +0530
categories: utterances jekyll blog
---

기존 jekyll 블로그 댓글서비스인 [Disqus][disqus]의 단점:
 
1. 무겁다
2. 광고가 나온다.(광고를 제거하기 위해서는 유료로 전환 필요)
3. 본인들 서비스에 로그인을 해야 댓글을 달 수 있다.

이 세가지 단점을 보완한게 [utterances][utterances]이다.


## utterances 서비스 방식
<hr>
utterances는 기본적으로 Github에 이슈를 만듬으로써, 댓글을 생성한다.
따라서 utterances가 Gihub에 이슈를 만들 수 있도록 Github와 연동및 권한을 부여해야 한다. 

![configure](../screenshot.png)

**Configure** 버튼 클릭
 

[disqus]: https://disqus.com
[utterances]: https://utteranc.es
