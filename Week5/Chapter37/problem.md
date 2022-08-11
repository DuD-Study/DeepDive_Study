# Chapter 37


<pre>1. 'minus'와 'plus'가 각각 몇번씩 출력되었을까요? </pre>

```js
function solution(arr)
{
  let answer = new Set(arr) 
  console.log(answer); // Set(5) { 5, 4, 3, 2, 1 }

  answer.forEach((v,i) => {
    if(v - i < 0) return console.log('minus');
    console.log('plus')
  })
  return answer;
}
let arr = [5,4,3,2,2,4,5,1,1];
console.log(solution(arr))
```

<details>
  <summary>Solution</summary>
  <pre>plus 5번 출력됩니다. 여기서의 forEach 메소드 첫번째 인수와 두번째 인수는 사실 같은 값을 
반환합니다. 일단 Set 객체는 순서가 의미가 없습니다. 즉 인덱스가 없음. 그런데도 왜 두번째 인수를 입력
받냐면, 배열에서의 forEach와 인터페이스를 통일시키기 위함이라고하네요. 그래서 v - i는 0입니다.</pre>
<details>

<br>