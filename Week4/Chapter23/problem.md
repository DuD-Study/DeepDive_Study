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

<pre>2. JS는 함수를 어디서 호출했는지가 아니라 어디에 정의했는지에 따라 상위 스코프를 결정하는데요,
이때 상위스코프는 어디에 저장될까요?</pre>



<details>
  <summary>Solution</summary>
  [[Environment]] 에 저장됩니다. 함수가 실행되면서 OuterLexicalEnvironmentRefrence를 통해 외부 렉시컬 환경을 참조하며 하나씩 거슬러 올라가게 됩니다.

</details>

<br>


