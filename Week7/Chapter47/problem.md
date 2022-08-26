# Chapter 47

<pre>1. 출력 값을 예상해보자.</pre>

```js
try {
    new Error("ERROR!")
} catch (err) {
    console.log(err)
} finally {
    console.log("finally")
}
```

<details>
  <summary>Solution</summary>
finally
  <pre>Error 생성자 함수로 에러 객체를 생성한다고 에러가 발생하진 않는다.<br>
throw new Error("ERROR!") 형식으로 에러를 발생 시켜줘야한다.</pre>
</details>

<br>
