this
-

[전역공간]
- window / global
 
[함수내부]
- window / global
 
[메소드 호출]
- 메소드 호출 주체

[callback func]
- 기본적으로는 함수의 this와 같다.
- 제어권을 가진 함수가 callback의 this를 명시한 경우 그에 따른다.
- 개발자가 this를 바인딩한 채로 callback을 넘기면 그에 따른다.

[생성자 함수]
- 인스턴스