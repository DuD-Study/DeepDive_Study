# Chapter 43

<pre>1. 다음은 HTTP 요청 전송 순서이다. 빈칸을 채워주세요</pre>

<pre>① XMLHttpRequest.prototype.[1.    ]메서드로 HTTP 요청을 초기화한다.<br>② 필요에 따라 XMLHttpRequest.prototype.[2.    ]메서드로 특정 HTTP 요청의 헤더 값을 설정한다.<br>③ XMLHttpRequest.prototype.[3.    ]메서드로 HTTP 요청을 전송한다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. open 2. setRequestHeader 3. send</strong>
  <pre>1. open메서드는 서버에 전송할 HTTP 요청을 초기화한다.<br>2. setRequestHeader메서드는 특정 HTTP 요청의 헤더 값을 설정하며, 반드시 open 메서드를 호출한 이후에 호출해야 한다.<br>3. send메서드는 open메서드로 초기화된 HTTP요청을 서버에 전송한다.</pre>
</details>

<br>


<pre>2. Ajax와 전통적인 방식과 비교했을때 장점 3가지 생각해보세요.</pre>

<details>
  <summary>Solution</summary>
  <pre>1) 필요한 데이터만 서버로부터 전송받아서, 불필요한 데이터 통신이 발생하지 않는다.
2) 변경할 필요 없는 부분은 재렌더링을 하지 않기때문에, 화면 깜박이는 현상이 없다.
3) 클라이언트와 서버와의 통신이 비동기 방식으로 동작하기 때문에 블로킹이 발생하지않는다.</pre>
</details>

<br>
<pre>3. [ ]은 클라이언트와 서버 간의 HTTP 통신을 위한 텍스트 데이터 포맷이다.</pre>

<details>
  <summary>Solution</summary>
  <pre>JSON</pre>
</details>

<br>
