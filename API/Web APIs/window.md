Web APIs > Window
-

[Size]
- window.screen : 모니터의 사이즈.
- window.outer : url + tab. 전체적인 브라우저의 사이즈.
- window.inner : 웹 페이지 + 스크롤바. 페이지가 표시되는 부분 전체.
- documentElement.client : 스크롤바를 제외한 문서 자체의 순수 사이즈.

[Scroll]
- window.scrollTo : 문서의 특정 좌표로 이동.
    - window.scrollTo(x-coord, y-coord)
    - window.scrollTo(options)
    
        
- window.scrollBy : 주어진 양만큼 창에서 문서를 스크롤.
    - window.scrollBy(x-coord, y-coord)
    - window.scrollBy(options)