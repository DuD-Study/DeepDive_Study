
# Chapter 4 

<pre>1. 자바스크립트는 변수의 타입 지정없이 값이 할당되는 과정에서 자동으로 변수의 타입이 결정된는데 이를 [          ]언어라고 한다.
</pre>

   <details>
      <summary>Solution</summary>
        <strong>동적타입</strong>
        
   </details> 

<br>
<br>
<br>




<pre>2. span3를 클릭하면 뭐라고 출력이 될까요?</pre>

```html
<body>
  <span id="span1">11</span>
  <span id="span2">22</span>
  <span id="span3">33</span>
  <span id="span4">44</span>
  <span id="span5">55</span>
</body>
```

```js
document.addEventListener('DOMContentLoaded', () => {
  console.log(`document's ready`);
  
  for(var i = 0; i < 5; i += 1){
    document.getElementById(`span${i+1}`).addEventListener('click', () => {
      console.log(i+1);
    })
  }
});
```


   <details>
      <summary>Solution</summary>
        <strong>6</strong>이다. 이유는 var는 블록 레벨 스코프를 따르지않는다. 거기다가 호이스팅 때문에 평가단계에서 var = i 는 함수 스코프내 코드맨위로 올라가는거나 다름없다. <br>그렇게 DOM이 로드되면 for문으로 5가 되고 그게 전역변수 형태니까 console.log(5+1) 이 되면서 6이 나온다.<br>let으로 바꿔주면 해결된다. let,const는 몸담고있는 블록 최상단까지만 간다.
   </details> 


<br>
<br>
<br>

<pre>3. 다음 실행결과를 예측해보세요.</pre>

```js
f1();

function f1(){
  console.log(y);
  function f2(){
    var y = 2;
    function f3(){
      console.log(y);
    }
    f3();
  }
  f2();
}
```


   <details>
      <summary>Solution</summary>
        <strong>y is not defined</strong> 외부에서 내부 함수의 변수는 접근 불가하다.
   </details> 