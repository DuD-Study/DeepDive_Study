# Chapter 39

<pre>1. HTMLCollection과 NodeList는 DOM API가 여러 개의 결과값을 반환하기 위한
DOM 컬렉션 객체입니다. 둘다 유사 배열 객체이면서 이터러블입니다. 둘의 차이가 뭘까요?</pre>

<details>
  <summary>Solution</summary>
  <pre>HTMLCollection 객체는 노드 객체의 상태 변화를 실시간으로 반영하는 살아 있는(live)<br/>DOM 컬렉션 객체입니다. 반대로 NodeList는 노드 객체의 상태 변경을 실시간으로 반영하지 않고 결과값을<br/>반환할때 그 상태를 정적으로 유지하는 죽은 (non-live) 객체로 동작합니다.하지만 안전하게 사용하려면<br/>둘다 Spread syntax 혹은 Array.from을 통해서 배열로 만들어 사용하라 하네요. (page 699)</pre>
</details>

<br>

<pre>2. HTML에서 Node와 Element 인터페이스를 상속받은 한 요소의 자식 요소를 탐색하려고 한다. 해당 노드를 반환하는건 같으나 차이점이 무엇일까요?</pre>

```js
Node.prototype.childNodes
Node.prototype.firstChild
Node.prototype.lastChild
------------------------------
Element.prototype.children
Element.prototype.firstElementChild
Element.prototype.lastElementChild
```

<details>
  <summary>Solution</summary>
  <pre>1. Node 인터페이스를 통한 탐색은 해당 자식 노드를 탐색하여 NodeList에 담아 반환을 합니다.<br/>   Element 인터페이스는 HTMLCollection에 담아 반환하죠.<br/><br/>2. Node 인터페이스는 요소노드뿐만 아니라 텍스트 노드도 포함되어 있을 수 있습니다.<br/>   하지만 Element 인터페이스는 텍스트 노드까지 반환하지 않아요.  </pre>
</details>

<br>

<pre>3. 다음 코드를 실행시 야기되는 문제점과 해결방안을 얘기해보자</pre>

```js
<head>
  <style>
    .red { color: red; }
    .blue { color: blue; }
  </style>
</head>
<html>
  <body>
    <ul id="fruits">
      <li class="red">Apple</li>
      <li class="red">Banana</li>
      <li class="red">Orange</li>
    </ul>
    <script>
      const $elems = document.getElementsByClassName('red');
        for (let i = 0; i < $elems.length; i++) {
        $elems[i].className = 'blue';
      }
    </script>
  </body>
</html>
```

<details>
<summary>Solution</summary>
위에 문제에서 설명한대로, getElementsByClassName이 반환하는 HTMLCollection 객체는 live DOM 컬렉션 객체이다. 그로인해 for문이 순환하는 과정에서 요소가 실시간으로 사라지므로 원하는 동작이 이루어 지지 않는다. 해결방안으로는 for문을 역순회하거나 while문으로 요소가 전부 사라질 때 까지 순회하는 방법이 있다.
</details>

<pre>4. 프로토타입 체인 관점에서, 파싱하여 객체화한 ul 요소 노드 객체에 바인딩된<br/>prototype을 모두 작성하세요.</pre>

<details>
  <summary>Solution</summary>
  <pre>HTMLUListElement, HTMLElement, Element, Node, EventTarget, Object의<br/>prototype에 바인딩되며 프로토타입 객체를 상속받는다.</pre>

</details>

<br>

<pre>5. Node.prototype.hasChildNodes 메서드는 자식 노드의 존재 유무에 따라 boolean을 반환하는데,<br>이때 텍스트 노드를 포함하여 자식 노드의 존재를 확인한다.<br>자식 노드 중에 텍스트 노드가 아닌 요소 노드가 존재하는지 확인할때 사용하는 프러퍼티를 작성하세요.</pre>

<details>
  <summary>Solution</summary>
  <pre>children.length 또는 Elemnent 인터페이스의<br> childElementCount 프러퍼티를 사용한다.</pre>
</details>

<br>

<pre>6. HTMLCollection 객체의 부작용을 막기위한 방법은 무엇이 있을까요? </pre>

<details>
  <summary>Solution</summary>
  <pre>querySelectorAll 메서드를 사용합니다 왜냐하면 DOM 컬렉션 객체인 NodeList 객체를 반환해주고 Nodelist 객체는 non-live 객체이다.</pre>
</details>

<br>

<pre>7. 정민이형은 왜이렇게 잘 생겼을까? </pre>

<details>
  <summary>Solution</summary>
  <pre><strong> abcddef </strong> asdf </pre>
</details>

<br>
