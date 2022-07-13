# Chapter 9
<h2 align="center">중요한 것은 코드를 예측할 수 있어야 한다는 것이다.</h2>
<br>

<pre>1. 개발자의 의도와는 상관없이 표현식 평가도중 JS엔진에 의해 암묵적으로 타입이 반환<br> 되는 경우가 있는데 이를 [          ] 또는 [          ] 라고 한다.</pre>
   <details>
      <summary>Solution</summary>
        <strong>암묵적 타입 변환, 타입 강제 변환</strong><br>
   </details> 
<br>
<pre>2. 표준 빌트인 생성자 함수는 3가지는 어떤것 일까요?</pre>
   <details>
      <summary>Solution</summary>
        <strong>String , Number, Boolean <br>
        보통 생성자 함수는 new 연산자를 호출하여 사용하는데 위의 3가지 생성자 함수는<br>
        String(1) -> "1" , Number('123') -> 123 , Boolean('x') // true, <br> 
        Boolean('') // false 이런식으로 변환이 가능합니다.</strong><br>
   </details> 
<br>

<pre>3. 'x' && 'y' 의 결과와 이유는?</pre>
   <details>
      <summary>Solution</summary>
        <strong>답은 y <br>
        이유 : 첫번째 x 는 true 로 평가되지만, 이 시점 까지는 표현식을 평가할수 없다.
        두 번째 피연산자까지 표현식의 평가 결과를 결정하는데 평과 결과를 결정할수 없어서<br> 
        논리 연산 결과를 결정하는 두 번째 피연산자 즉 문자열 'y'를 그대로 반환합니다.</strong><br>
   </details> 
<br>




