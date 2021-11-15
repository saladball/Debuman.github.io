---
layout: post
title: “Formspree를 사용하여 Jekyll블로그에서 메일 전송”
date: 2021-11-15 15:05:00 +0530
categories: formspree jekyll blog email
---

## Formspree
<hr>
<br>
정적인 서비스인 Github 블로그에서는 서버를 통한 이메일을 발송하는 기능을 구현할 수 없다. 하지만 이런 정적 서비스에서 이메일 전송을 가능하도록 도와주는 서비스가 바로 오늘 설치할 [Formspree][formspree]이다.
Formspree를 사용하여 jekylld에서 이메일을 발송하는 기능을 구현해보겠다.
<br>

![Signup](/../image/2021/11/15/"signup.png")
먼저 [Formspree][formspree]에 접속하고 **Get start**를 클릭하여 회원가입을 진행한다.
<br>

![Formbutton](/../image/2021/11/15/"Formbutton.png")
회원가입후 이메일 인증까지 완료한 후 아래 생성된 본인의 스크립트 중에 본인이 원하는 기능이 있는 스크립트를 선택 후 복사한다. 필자는 버튼생성을 위해 **Formbutton** 스크립트를 선택하였다.
<br>
이후 복사한 스크립트를 본인의 Jekyll블로그에 추가하여 화면에 표시하도록 하자. 자신의 테마에서 블로그에 표시하는 템플리슬 찾아 복사한 스크립트를 추가한다. 필자는 [PlainWhite][plainwhite]테마를 사용중 이므로 **_layouts/post.html** 파일에 추가하였다.
<br>
![complete](/../image/2021/11/15/"complete.png")
이후 정상적으로 자신의 Jekyll블로그에 표시되는 것을 확인할 수 있다.

