# Chapter 17

<pre>1. 아래 4가지가 일급 객체임을 만족하는 조건이다. 빈칸을 채워보자.</pre>

<div align="center">
1. 무명의 [___]로 생성할 수 있다. 즉 런타임에 생성이 가능하다. <br>
2. 변수나 [____]에 저장할 수 있다. <br>
3. 함수의 [____]에 전달할 수 있다. <br>
4. 함수의 [___]으로 사용할 수 있다. <br>
</div>

<details>
  <summary>Solution</summary>
  <strong>
  1. 리터럴  ex) function(x, y) {return x*y} <br></strong>
  
  ```js
  const af = function() {
    return alert('anonymous function')
  }
  af();
  ```

  <strong>2. 자료구조 (객체, 배열) <br>
  3. 매개변수</strong><br>

  ```js
  function foo(x) {
    alert(x);
  }
  function bar(func) {
    func("Hello World!");
  }
  bar(foo);
  ```
  <strong>4. 반환값 <br> </strong>
  
  ```js
  function a(){
  return b();
}

function b(){
  alert('Hello World');
}
a();
  ```
</details>

<br>
