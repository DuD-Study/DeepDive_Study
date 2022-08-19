# Chapter 38

<pre>1. 노드 추가/삭제, 요소의 크기/위치 변경, 윈도우 리사이징 등 레이아웃에 영향을 주는 변경이 
발생한 경우 다시 계산을 하는 것을 [     1     ] 라고 하며, 재결합된 렌더 트리를 기반으로
다시 그리는 것을 [    2     ]라고 한다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1.리플로우(reflow)
  <br/>2.리페인트(repaint)</strong>
  <pre>페이지 673쪽 참고해 주십쇼오...</pre>
</details>

<br>

<pre>2. script어트리뷰트 중 이 어트리뷰트들은 자바스크립트 파싱에 의한 DOM 생성이<br>중단되는 문제를 근본적으로 해결하기 위해 HTML5부터 추가되었으며,<br>HTML 파싱과 외부 자바스크립 파일의 로드가 비동기적으로 진행된다.<br>[1.     ] 어트리뷰트는 로드가 왼료된 자바스크립트부터 먼저 실행되어 DOM생성 완료 전에 해당 script가 실행될 수 있으며,<br>[2.     ] 어트리뷰트는 DOM 생성이 완료된 직후 해당 script가 실행된다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. async 어트리뷰트
  <br/>2. defer 어트리뷰트</strong>
  <pre>async 어트리뷰트는 IE10이상에서 지원하며,<br>defer 어트리뷰트는 IE10이상에서 지원하고, IE6 ~ IE9에서도 지원하지만 정상적으로 동작하지 않을 수 있다.</pre>
</details>

<br>
