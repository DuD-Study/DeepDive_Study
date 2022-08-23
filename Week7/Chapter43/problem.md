# Chapter 43

<pre>1. 다음은 HTTP 요청 전송 순서이다. 빈칸을 채워주세요</pre>

<pre>① XMLHttpRequest.prototype.[1.    ]메서드로 HTTP 요청을 초기화한다.<br>② 필요에 따라 XMLHttpRequest.prototype.[2.    ]메서드로 특정 HTTP 요청의 헤더 값을 설정한다.<br>③ XMLHttpRequest.prototype.[3.    ]메서드로 HTTP 요청을 전송한다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. open 2. setRequestHeader 3. send</strong>
  <pre>1. open메서드는 서버에 전송할 HTTP 요청을 초기화한다.<br>2. setRequestHeader메서드는 특정 HTTP 요청의 헤더 값을 설정하며, 반드시 open 메서드를 호출한 이후에 호출해야 한다.<br>3. send메서드는 open메서드로 초기화된 HTTP요청을 서버에 전송한다.</pre>
</details>

<br>
