# Chapter 44

<pre>1. Rest Api를 구성하는 3가지 요소와 각 요소들의 표현방법을 간단하게 작성하세요.</pre>

<details>
  <summary>Solution</summary>
  <pre>구성요소 3가지는 자원, 행위, 표현이며 각각의 표현방법은 URL(엔드포인트), HTTP요청 메서드, 페이로드이다.</pre>
</details>

<br>

<pre>2. 빈칸을 채워보시오. </pre>

|HTTP 요청 메소드|종류|목적|페이로드|
|:-:|:-:|:-:|:-:|
|GET|index/retrieve|모든/특정 리소스 취득|(1)|
|POST|create|리소스 생성|O|
|(2)|replace|(3)|O|
|(4)|modify|(5)|(6)|
|DELETE|delete|모든/특정 리소스 삭제|X|

<details>
  <summary>Solution</summary>
  <pre>(1) X 
(2) PUT
<strong>(3) 리소스 전체 교체 </strong>
(4) PATCH 
<strong>(5) 리소스 일부 수정</strong>
(6) O</pre>
</details>

<br>
