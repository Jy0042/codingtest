<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. n의 배수</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(num, n) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*정수 `num`과 `n`이 매개 변수로 주어질 때, `num`이 `n`의 배수이면 1을 return `n`의 배수가 아니라면 0을 return하도록 solution 함수를 완성해주세요.*<br />


---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(num, n) {
    //num % n 의 값이 0일 때는 정확하게 비교하고 삼항연산자를 사용하여 처리
    const answer = num % n === 0 ? 1 : 0;
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>앞서 배운 삼함연산자를 이용하여 처리하였다

>`"=="` 연산자는 느슨한 동등 비교(Loose Equality Comparison)를 수행합니다.<br /> 
이 연산자를 사용하면 두 값이 같은 값으로 간주되는 조건이 몇 가지 있습니다.<br />
>   * 두 값이 같은 자료형이면 값의 내용이 같아야 합니다.<br />
>   * 두 값이 다른 자료형이면 자동으로 타입 변환을 수행하여 비교합니다.
<br />

>`"==="` 연산자는 엄격한 동등 비교(Strict Equality Comparison)를 수행합니다. <br />이 연산자를 사용하면 두 값이 완전히 같은지 비교하며, 자료형과 값이 모두 같아야 true를 반환합니다. 

>~~조금씩 늘어가고 있는 거 같다..~~

</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 홀짝에 따라 다른 값 반환하기</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(n) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*양의 정수 n이 매개변수로 주어질 때, n이 홀수라면 n 이하의 홀수인 모든 양의 정수의 합을 return 하고 n이 짝수라면 n 이하의 짝수인 모든 양의 정수의 제곱의 합을 return 하는 solution 함수를 작성해 주세요.*


---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1">

```javascript
function solution(str1, str2) {
    
    var answer = '';
    
    // 반복문으로 두 매개변수의 문자열을 더한 값만큼 실행
    for (let i = 0; i < str1.length; i++) {
        answer += str1[i] + str2[i];
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`더하기 할당 연산자(+=)` 는 오른쪽 피연산자의 값을 변수에 더한 결과를 다시 변수에 할당

>`거듭제곱 연산자(**)`는 왼쪽 피연산자를 밑, 오른쪽 피연산자를 지수로 한 값을 구한다


</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. 조건 문자열</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(ineq, eq, n, m) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*문자열에 따라 다음과 같이 두 수의 크기를 비교하려고 합니다.

두 수가 `n`과 `m`이라면<br />

* ">", "=" : `n` >= `m`<br />
* "<", "=" : `n` <= `m`<br />
* ">", "!" : `n` > `m`<br />
* "<", "!" : `n` < `m`<br />

두 문자열 `ineq`와 `eq`가 주어집니다. `ineq`는 "<"와 ">"중 하나고, `eq`는 "="와 "!"중 하나입니다. 그리고 두 정수 `n`과 `m`이 주어질 때, `n`과 `m`이 `ineq`와 `eq`의 조건에 맞으면 1을 아니면 0을 return하도록 solution 함수를 완성해주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(ineq, eq, n, m) {
    var answer = 0;
    // 조건문으로 각 변수를 비교 
    if ((ineq === ">" && n > m ) || (ineq === "<" && n < m) || (ineq === "!" && n !== m)) {
        answer = 1;    
    } else if ((eq === "=" && n === m)) {
        answer = 1;
    }
      
    return answer;
}

```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>조건문의 `논리연산자 AND (&&)`를 사용하여 모든 연산이 참일 때의 조건을 

> `OR(||)`  인수 중 하나라도 true이면 true를 반환하고, 그렇지 않으면 false를 반환


</div>
</details>


------
<br /><br />
---
