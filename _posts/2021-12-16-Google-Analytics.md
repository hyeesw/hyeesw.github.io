---
layout: single
title:  Google Analytics
---

## Google Analytics 추가하기  

hyeesw.github.io가 잘 나오는 상태로 준비한다.  
<https://analytics.google.com/analytics/web/> 에 접속해서 회원가입을 한다.  
회원가입이 끝나면 아래와 같은 창이 뜬다.  
![image](https://user-images.githubusercontent.com/84231143/146367357-31696d17-135c-447a-80c3-1e21ddfe598a.png)

위 창에서 **웹**을 눌러, 내 **git page**의 **url**을 입력하고 스트림 이름은 원하는 이름을 입력한다.  
**스트림을 만들기** 버튼을 누르면 아래와 같은 창이 뜨는데, 빨강색 박스 안의 **측정 ID**를 복사한다.  
![image](https://user-images.githubusercontent.com/84231143/146380393-3826bc17-3839-43a5-9577-7a5f24769e5c.png)  

git으로 가서 **\_config.yml** 의 **analytics:** 부분의 코드를 찾아, 아래와 같이 수정한다.  
>provider: “google-gtag”  
>traking_id: 측정ID 복붙 (큰 따옴표로 묶는다)  
>anoymize_ip: false 

아래 사진을 참고하자!  
![image](https://user-images.githubusercontent.com/84231143/146369654-e83e26e8-a003-4454-ae38-fbe25b262e24.png)

**Google Analytics 추가가 끝났다!**  
이제 <https://analytics.google.com/analytics/web/> 접속해서  
**보고서 개요**를 클릭하면,아래 사진과 같이 방문자수, 유입경로 등 여러 정보를 볼 수 있다.
![image](https://user-images.githubusercontent.com/84231143/146370032-49ee381e-b924-4554-be7c-07e08c5f149b.png)
