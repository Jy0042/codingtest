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
function solution(n) {
    var answer = 0;
    // 조건문으로 n 이 홀수일때를 판별
    if ( n % 2 === 1 ) {
        // 반복문으로 n 이 홀수면 i를 1 로 할당하고 n 보다 작거나 같을 때까지 +2씩 증가
        for (let i = 1; i <= n; i += 2) {
            // 반복문의 조건의 부합한 모든 값을 더한 값 i를 answer에 추가
            answer += i
        }
    // 또 다른 조건으로 n 이 짝수일때
    } else if ( n % 2 === 0 ) {
        // 반복문으로 n이 짝수면 i를 2로 할당하고 n 보다 작거나 같을 때까지 +2씩 증가
        for (let i = 2; i <= n; i += 2)
            // 조건에 부합한 모든 i 는 2제곱을 한 뒤 값을 더해 answer 에 추가
            answer += i**2
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

## <p style="color:yellow;">4. 코드 처리하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(code) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*문자열 `code`가 주어집니다. <br />
<br />
`code`를 앞에서부터 읽으면서 만약 문자가 "1"이면 `mode`를 바꿉니다. `mode`에 따라 `code`를 읽어가면서 문자열 `ret`을 만들어냅니다.<br />
`mode`는 0과 1이 있으며, `idx`를 0 부터 `code의 길이 - 1` 까지 1씩 키워나가면서 `code[idx]`의 값에 따라 다음과 같이 행동합니다.<br />
<br />
`mode`가 0일 때<br />
`code[idx]`가 "1"이 아니면 `idx`가 짝수일 때만 `ret`의 맨 뒤에 `code[idx]`를 추가합니다.<br />
`code[idx]`가 "1"이면 `mode`를 0에서 1로 바꿉니다.<br />
`mode`가 1일 때<br />
`code[idx]`가 "1"이 아니면 `idx`가 홀수일 때만 `ret`의 맨 뒤에 `code[idx]`를 추가합니다.<br />
`code[idx]`가 "1"이면 `mode`를 1에서 0으로 바꿉니다.<br />
문자열 `code`를 통해 만들어진 문자열 `ret`를 return 하는 solution 함수를 완성해 주세요.<br />
<br />
단, 시작할 때 `mode`는 0이며, return 하려는 `ret`가 만약 빈 문자열이라면 대신 "EMPTY"를 return 합니다.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(code) {
    let ret = '';
    
    // mode의 초기값 설정
    let mode = 0;
    
    for (let i = 0; i < code.length; i++) {
        // 조건문으로 mode의 값을 설정
        if (mode === 0) {
            if (code[i] !== "1" && i % 2 === 0) {
                ret += code[i];
            } else if (code[i] === "1") {
                mode = 1;
            }
        } else if (mode === 1) {
             if (code[i] !== "1" && i % 2 === 1) {
                ret += code[i];
            } else if (code[i] === "1") {
                mode = 0;
            }
        }
    }
    if (ret === '') {
        ret = "EMPTY";
    }
    return ret;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>조건문 너무 난잡한거 같아서 다른 방법의 풀이를 찾아보니

```javascript
if (code[i] === "1") {
      mode = 1 - mode;
    } else if ((mode === 0 && i % 2 === 0) || (mode === 1 && i % 2 === 1)) {
      ret += code[i];
    }
```
>이렇게 조건문을 짤수도 있었다<br />
초기 `mode` 의 값을 `0`으로 설정했으니 추가 조건문에서 값을 할당하여 간단하게 처리할 수 있었다
</div>
</details>


---
<br /><br />
---
## <p style="color:yellow;">5. 등차수열의 특정한 항만 더하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, d, included) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*두 정수 `a`, `d`와 길이가 n인 boolean 배열 `included`가 주어집니다. 첫째항이 `a`, 공차가 `d`인 등차수열에서 `included[i]`가 i + 1항을 의미할 때, 이 등차수열의 1항부터 n항까지 `included`가 true인 항들만 더한 값을 return 하는 solution 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(a, d, included) {
    var answer = 0;

    // 반복문으로 included 의 배열의 길이 까지 실행
    for (let i = 0; i < included.length; i++) {
        // 조건문으로 included index가 true 일 때
        if (included[i]) {
            answer += a + i * d;
        }
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>문제의 수열을 알고있다면 쉬울수도...
</div>
</details>


---