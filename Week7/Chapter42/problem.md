# Chapter 42

<pre>1. 현재 실행 중인 태스크가 종료할 때까지 다음에 실행될 태스크가 대기하는 방식을 [1.     ]라고 한다.<br>2. 현재 실행 중인 태스크가 종료 되지 않은 상태라 해도 다음 태스크를 곧바로 실행하는 방식을 [2.     ]라고 한다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. 동기 처리 2. 비동기 처리</strong>
  <pre>동기 처리방식은 실행 순서가 보장된다는 장점이 있지만, 앞선 태스크가 종료할 때까지 이후 태스크들이 블로킹된다는 단점이 있다.<br>비동기 처리방식은 블로킹이 발생하지 않는다는 장점이 있지만 실행 순서가 보장되지 않는 단점이 있다.</pre>
</details>

<br>

<pre>2. 자바스크립트 엔진은 한 번에 하나의 태스크만 실행할 수 있는 [    1    ] 방식으로 동작합니다.
   그래서 하나의 태스크만 실행할 수 있기 때문에 시간이 걸리는 태스크 실행 시 [    2    ] 가 발생합니다. </pre>

<details>
  <summary>Solution</summary>
  <strong>1. 싱글 스레드(single thread) 2. 블로킹(blocking)</strong>
  <pre>자세한건 페이지 810</pre>
</details>

<br>
<pre>3. HTML 요소가 애니메이션 효과를 통해 움직이고 이벤트를 처리하기도 하고, HTTP요청을 통해 서버로부터 데이터를 가지고오면서 렌더링 하는건 무엇일까요? </pre>

<details>
  <summary>Solution</summary>
  <pre>이벤트 루프
  P.813 참고</pre>
</details>

<br>

<pre>4. 아래는 무엇을 설명하는 것인가?</pre>

<pre><strong>이것</strong>은 객체가 저장되는 메모리 구조이다.<br>
콜 스택의 요소인 실행 컨텍스트는 <strong>이것</strong>에 저장된 객체를 참조한다.<br>
메모리에 값을 저장하려면 먼저 값을 저장할 메모리 공간의 크기를 결정해야한다.<br>
객체는 원시 값과는 달리 크기가 정해져 있지 않으므로 할당해야할 메모리 공간의 크기를 런타임에 결정(동적 할당)해야 한다.<br>
따라서 객체가 저장되는 메모리 공간인 <strong>이것</strong>은 구조화 되어있지 않다는 특징이 있다.</pre>

<details>
<summary>Solution</summary>
<Strong>힙(heap)</Strong>
</details>
