---
layout: single
title: "change favicon!"
comments: true
---

# change favicon


<https://icons8.kr/icons/set/favicon-ico> 에서 원하는 favicon 이미지를 pc에 저장한다.

<https://www.favicon-generator.org/> 에 들어가서 **파일 선택** 을 누르고 pc에 저장한 favicon을 불러온다.  
**create favicon** 버튼을 누르면 아래와 같이 뜰 것이다.

![image](https://user-images.githubusercontent.com/84231143/146337026-ace63af2-8d41-4893-aeb7-7a08d069b591.png)

**Download the generated favicon**을 눌러 다운 받는다.

**git**으로 가서 **assets** 디렉토리 아래 **logo.ico** 디렉토리를 만들어준다. 

**logo.ico** 디렉토리에 안에 다운 받은 파일의 압축을 풀어서 넣는다.

이번에는 **\_includes** 디렉토리에 들어가 **head.html** 파일을 찾는다.

아래 코드들을 복사하여 **head.html** 코드 맨 아래줄에 추가한다.
![image](https://user-images.githubusercontent.com/84231143/146337695-169dbd55-0f53-4ff7-984d-6c1117509d3a.png)

이때 복사한 코드를 살펴보면 아래처럼 적혀있는데,
`<link rel="apple-touch-icon"  sizes="57x57" href="/apple-icon-57x57.png">`  
코드에 **href="/** 부분이 있는 줄은 모두 약간의 수정이 필요하다.  
`\{{site.baseurl}}/assets` 를 아래 사친처럼 사이에 끼워준다.  
![image](https://user-images.githubusercontent.com/84231143/146383344-339da8ba-0038-47f6-89a2-09411522a362.png)

**href**가 적혀있는 모든 곳에 위와 같이 추가하고, **commit**하면 favicon 변경 끝!
