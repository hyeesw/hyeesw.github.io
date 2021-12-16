---
layout: single
title: "How to install jekyll?"
comments: true
---

## Jekyll이란?
Ruby에 기반한 정적 웹사이트 생성 프레임워크
# Jekyll을 이용해서 git page를 만들어 보자!
### <페이지 만들기>
---------------
1. `jekyll new . –force`  :  만들고자 하는 로컬 리포지토리에 지킬 설치
2. `bundle exec jekyll serve` 로컬 서버 동작

__<아래 과정은 원격 리포에 반영하는 방법입니다.>__
3. `git rm index.html`  이 파일을 삭제하면 이전에 있던 페이지를 없애고 새로운 페이지로 갱신한다.
4. `git add *`
5. `git commit –m “add: blog”`
6. 6. `git push origin main` <<username.github>>.github.io 에 가보면 원격으로도 반영이 된 것을 확인할 수 있다.

### <포스트 업로드>
---------------
1. _posts 파일 안에 YYYY-MM-DD-TITLE.md 파일을 새로 열고
2. 그 안에 markdown 형식으로 내용을 작성한다.
3. 위에서 언급한 방식으로 local에 commit으로 반영한 후 `git push origin main` 하면 원격 리포에도 반영 됨을 확인할 수 있다.

### <댓글 기능 추가>
---------------
1. <<username>>.github.io가 잘 나오는 상태로 준비한다.
2. https://disqus.com 에 들어가서 로그인 후 strat를 누른다.
3. “I want to install Disqus on my site” 를 누른다.
4. 정보를 입력하되, Website name은 꼭 기억하기!
5. 뒤로 가다보면 wetsite URL 부분이 있는데 거기에 https://<<username>>.github.io 를 입력한다.

__<아래 과정은 파일에 반영하는 방법입니다.>__

6. \_config.yml 파일을 열어 아래 사진과 같이 추가한다. 
 (만약 아래 틀을 가지고 있는 테마라면 따로 추가하지 말고 해당 부분을 수정한다. )
 
![image](https://user-images.githubusercontent.com/84231143/146325304-aaa2b00c-cce9-4729-bd2b-2d74b0bba981.png)

7. disqus 홈피에 있는 code 복사
8. \_layouts/post.html에 복사한 코드를 아래 if문으로 묶기
{% if page.comments %}
{% endif %}

9. 주석 해제 후, 아래 두 코드를 추가한다.
let PAGE_URL = “{{site.url}}{{page.url}}”
let PAGE_IDENTIFIER = “{{page.url}}”

10. `s.src = ‘https://<<username>>.disqus.com/embed.js’;` 잘 나와있는지 확인
11. \_posts 폴더 아래 댓글 기능을 허용하고 싶은 **.md 파일**에 `comments: true`로 설정한다.
