# Chapter 23

<pre>1. 실행 컨텍스트를 생성하는 4가지의 소스코드 타입은 ?</pre>

<details>
  <summary>Solution</summary>
  <strong>1. 전역 코드 - 전역에 존재하는 소스코드를 말하고, 함수, 클래스의 내부 코드는 포함 x <br>
  2. 함수 코드 - 함수 내부에 존재하는 소스코드를 말하고, 중첩함수, 클래스의 내부 코드는 포함 x <br>
  3. eval 코드 - 빌트인 전역 함수인 eval 함수에 인수로 전달되어 실행되는 소스코드  <br></strong>
  4. 모듈 코드 - 모듈 내부에 존재하는 소스코드, 내부의 함수, 클래스 내부 코드는 포함 x<br>
</details>

<br>


<pre>2. 빈칸에 들어갈 알맞은 단어를 쓰십시오.</pre>

<pre> 실행 컨텍스트 스택은 코드의 실행 순서를 관리하며,<br>실행 컨텍스트 스택의 [    ]에 존재하는 실행 컨텍스트는 언제나<br> 현재 실행 중인 코드의 실행 컨텍스트다. 
</pre>

<details>
  <summary>Solution</summary>
  <strong>최상위</strong>
  <pre>소스코드가 평가되면 실행 컨텍스트가 생성되고 실행 컨텍스트 스택의 최상위에 쌓인다.</pre>
</details>

<pre>3. JS는 함수를 어디서 호출했는지가 아니라 어디에 정의했는지에 따라 상위 스코프를 결정하는데요,
이때 상위스코프는 어디에 저장될까요?</pre>



<details>
  <summary>Solution</summary>
  [[Environment]] 에 저장됩니다. 함수가 실행되면서 OuterLexicalEnvironmentRefrence를 통해 외부 렉시컬 환경을 참조하며 하나씩 거슬러 올라가게 됩니다. 참고 페이지 379P

</details>

<br>

<pre>4. var 키워드로 선언한 전역변수와 let, const 키워드로 선언한 전역 변수는 각각 전역 확경 레코드의 어떤 레코드에 저장되는가?</pre>

<details>
<summary>Solution</summary>
var 키워드 - 객체 환경 레코드(Object Environment Record)<br>
let, const 키워드 - 선언적 환경 레코드(Declarative Environment Record)</details>



<br>
