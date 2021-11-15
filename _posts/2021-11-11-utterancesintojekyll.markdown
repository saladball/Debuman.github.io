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

![configure](/../image/2021/11/configure.png)

**Configure** 버튼 클릭
 
![RepositorySave](/../image/2021/11/RepositorySave.png)

Github 계정 로그인 후 댓글 기능(utterances)을 사용할 **Repository**를 선택

utterances가 Github의 이슈를 생성하 도록 설정 후 이 이슈들을 화면에 표시하도록 utterances의 스크립트를 생성.

utterances의 스크립트를 생성하기 위해 [공식 페이지][utterances]로 이동

![Repo](/../image/2021/11/Repo.png)

이동 후 **Repository**를 입력하는 화면에서 앞에서 이슈를 생성할 수 있게 권한을 부여한 저장소를 [User Name]/[Repository] 형식으로 작성.

![BlogPost](/../image/2021/11/BlogPost.png)

Repo 작성 후 하단 **Blog Post ↔️  Issue Mapping** 은 크게 중요하지 않지만 Github 이슈화면에서 댓글이 어떻게 보일 것인지를 설정하는 것이므로 자신에게 맞는 항목을 선택.

![IssueLabel](/../image/2021/11/IssueLabel.png)

다음 Issue Label 항목은 Github에 이슈가 생성될 때, 다른 이슈와 구별하기 위해 라벨링을 하는 옵션이지만 따로 설정하지 않고 진행.

![Theme](/../image/2021/11/Theme.png)

Theme 항목에서는 자신의 블로그의 테마에 맞는 옵션을 선택한다. 

![Script](/../image/2021/11/Script.png)

모든 항목을 자신의 블로그에 맞게 선택하였으면, 하단 Enable Utterances 항목에서 자신의 utterances 스크립트가 생성된 것을 확인할 수 있다.

## Jekyll 블로그에 적용
<hr>
이렇게 생성한 스크립트를 Jekyll블로그에 추가하여 화면에 표시해 보자.
필자는 [PlainWhite][plainwhite]테마를 사용하고 있다. 
자신의 테마에서 블로그에 표시하는 템플릿을 찾아 복사한 스크립트를 추가한다.
필자는 **_layouts/post.html** 파일에 추가하였다.

이로써 utteracnes을 사용하여 Jekyll 블로그에 댓글 기능을 추가하였다.
이제 추가한 내용이 잘 적용되었는지 확인하기 위해 다음 명령어를 실행하여 Jekyll블로그를 실행해보자.
```
bundle exec jekyll serve
```

문제없이 잘 실행되었다면, 블로그 페이지에 다음과 같이 utterances 댓글 기능이 표시되는 것을 확인할 수 있다.

![Complete](/../image/2021/11/Complete.png)


[disqus]: https://disqus.com
[utterances]: https://utteranc.es
[plainwhite]: https://github.com/samarsault/plainwhite-jekyll 
