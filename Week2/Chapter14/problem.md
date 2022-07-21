# Chapter 14

<pre>1. [     ]는 코드가 실행되기 이전 단계에 자바스크립트 엔진에 의해 어떤 객체보다도 먼저 생성되는 특수한 객체다.<br>[     ]는 클라이언트 사이드 환경(브라우저)에서는 window, 서버사이드 환경(Node.js)에서는 global객체를 의미한다.</pre>

<details>
  <summary>Solution</summary>
    <strong>전역 객체(global object)</strong> : 전역 객체는 표준 빌트인 객체와 환경에 따른 호스트 객체(클라이언트 Web API 또는 Node.js의 호스트 API), 그리고 var키워드로 선언한 전역 변수와 전역 함수를 <strong>프로퍼티로 갖는다.</strong>
</details>

<br>

<pre>2. 변수는 선언에 의해 생성되고 할당을 통해 값을 갖는다. 그리고 언젠가는 소멸되는데 이것을 과정을 변수의 [         ]라고 한다. 전역 변수의 [            ]는 애플리케이션의 [         ]와 같다.</pre>

<details>
  <summary>Solution</summary>
    <strong>생명주기 (Life Cycle)</strong>
</details>

<br>

<pre>3. 전역 변수의 문제점을 설명하시오. (4가지)</pre>

<details>
  <summary>Solution</summary>
    <strong>암묵적 결합(implicit coupling)</strong>: 전역 변수를 선언한다는 것은 코드 어디서든 참조하고 할당할 수 있는 변수를 사용하겠다는 의미를 담고 있기 때문에 유효 범위가 크면 코드의 가독성이 나빠지고 의도치 않게 상태가 변경되어 위험성이 높아진다.<br>
    <strong>긴 생명주기</strong>: 메모리 리소스를 오랜시간 소비함.<br>
    <strong>스코프 체인상 종점에 존재</strong>: 검색속도가 느림.<br>
    <strong>네임스페이스 오염</strong>: 다른 파일 내 동일한 이름으로 명명된 전역 변수/함수가 같은 스코프 내 존재할 경우 예상치 못한 결과 발생.
</details>

<br>
