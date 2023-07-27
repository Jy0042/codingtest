<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. 문자열 겹쳐쓰기</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(my_string, overwrite_string, s) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*문자열 `my_string`, `overwrite_string`과 정수 `s`가 주어집니다. <br />문자열 `my_string`의 인덱스 `s`부터 `overwrite_string`의 길이만큼을<br /> 문자열 `overwrite_string`으로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.*<br />

__*[출력 예시]*__<br />
```
!@#$%^&*(\'"<>?:;
```

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(my_string, overwrite_string, s) {
    // 매개변수들의 문자열의 길이를 저장하는 지역 변수 선언
    const oslen = overwrite_string.length;
    // substring 사용해 문자열의 인덱스 0 부터 변수 s 직전까지의 부분 문자열과 
    // overwrite_string 문자열을 합치고
    // substring 사용해 문자열의 인덱스 변수 s 부터 overwrite_string 의 
    // 문자열 갯수를 담고 있는 변수 oslen 직전까지의 my_string 와 합친다
    const answer = (my_string.substring(0,s) + overwrite_string + my_string.substring(s + oslen));

    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`my_string` 의 인덱스가 `overwrite_string` 의 인덱스보다 클 때는 문제가 없었지만 작았을 때 `overwrite_string` 를 합치고 남은 `my_string` 의 문자열의 인덱스가 문제였다..<br />
결국 검색을 통해 해결하였다.. <br />
~~나는 왜 `my_string.substring(s + oslen)` 이 부분을 생각하지 못하였을까...~~

>`slice()` 메서드를 이용한 풀이도 가능하다.

</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 문자열 섞기</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(str1, str2) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*길이가 같은 두 문자열 `str1`과 `str2`가 주어집니다.<br />
<br />
두 문자열의 각 문자가 앞에서부터 서로 번갈아가면서 한 번씩 등장하는 문자열을 만들어 return 하는 solution 함수를 완성해 주세요.*
<br /><br />
*[제한사항] <br />
1 ≤ str1의 길이 = str2의 길이 ≤ 10*


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

>반목문의 바깥쪽에 변수를 선언하고 초기화를 해놓으면 각 반복에서 결과 값을 누적하여 저장

>`()` 와 `[]` 의 차이점은 `()` 는 함수를 호출 시에 사용 <br />
`[]` 는 배열을 생성하거나 배열 요소에 접근할 때 사용


</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. 문자 리스트를 문자열로 변환하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(arr) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*문자들이 담겨있는 배열 `arr`가 주어집니다. <br />`arr`의 원소들을 순서대로 이어 붙인 문자열을 return 하는 solution함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(arr) {
    
    var answer = '';
    
    // 반복문으로 배열의 문자열 길이만큼 실행 되게 하고
    for (let i = 0; i < arr.length; i++)
        
        // 실행된 값을 answer에 추가
        answer += arr[i];
    
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>다른 방법으로 풀 수 있는 지 찾아보았다

>`join()` 메서드를 사용하여 푸는 방법도 있었다

```javascript
function solution(arr) {
    
    var answer = arr.join('');
    
    return answer;
}
```
>>결합할 때 `구분자`를 사용하지 않으면 기본적으로 `쉼표(,)` 로 구분되어 결합 <br />
구분자로 `빈 문자열 ('')`을 지정하면 `배열의 요소들이 붙어서 하나의 긴 문자열`로 결합



</div>
</details>


------
<br /><br />
---

## <p style="color:yellow;">4. 더 크게 합치기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, b) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다.*<br />
*예를 들면 다음과 같습니다.*<br />

>12 ⊕ 3 = 123 <br />
>3 ⊕ 12 = 312 <br />

*양의 정수 `a`와 `b`가 주어졌을 때, `a` ⊕ `b`와 `b` ⊕ `a` 중 더 큰 값을 return 하는 solution 함수를 완성해 주세요.<br />
<br />
단, `a` ⊕ `b`와 `b` ⊕ `a`가 같다면 `a` ⊕ `b`를 return 합니다.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(a, b) {
    var answer = 0;
    // 조건문으로 a ⊕ b 와 b ⊕ a 를 비교
    if (`${a}${b}` >= `${b}${a}`) {
        answer = `${a}${b}`;
    } else {
        answer = `${b}${a}`;
    }
    // 값을 숫자형으로 변환
    return Number(answer);
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>다른 방법의 풀이를 찾아보니

```javascript
function solution(a, b) {
    return Math.max(Number(`${a}${b}`), Number(`${b}${a}`))
}
```
>이 방법의 풀이가 인상 깊었다

>`Math` 는 JavaScript의 `내장 객체(Object)`로, 수학적인 연산을 수행하기 위한 다양한 속성과 메서드를 제공하는 정적(Static) 객체<br />
`Math` 는 Number 자료형만 지원하며 BigInt와는 사용할 수 없다

>`Math.max` 함수는 인자로 `주어진 숫자들 중에서 가장 큰 값을 반환`하는 JavaScript의 내장 함수입니다.<br /> 이 함수는 매개변수로 전달된 숫자들 중에서 최댓값을 찾아 반환하며, 매개변수는 쉼표로 구분하여 여러 개를 동시에 전달할 수 있다
</div>
</details>


---
<br /><br />
---
## <p style="color:yellow;">5. 두 수의 연산값 비교하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, b) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.*

>12 ⊕ 3 = 123<br />
3 ⊕ 12 = 312

*양의 정수 `a`와 `b`가 주어졌을 때, `a` ⊕ `b`와 `2 * a * b` 중 더 큰 값을 return하는 solution 함수를 완성해 주세요.<br />
단, `a` ⊕ `b`와 `2 * a * b`가 같으면 `a` ⊕ `b`를 return 합니다.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(a, b) {
    // a 와 b를 ``로 연결하고 다시 숫자형으로 변환한 값을 AB에 할당
    const AB = Number(`${a}${b}`);
    const BA = 2*a*b;
    // 삼항연산자를 사용해 조건이 참일때 와 거짓일 때의 값을 설정
    return AB >= BA ? AB : BA;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>4번 문제랑 거의 비슷해서 `Math.max` 를 사용해서 풀려고 하였으나, 문제를 보디 값이 같을 때의 조건도 있어서 4번의 `Math.max`의 풀이가 잘못됐다는 걸 알았다

>`삼항연산자` 세 개의 피연산자를 받는 유일한 연산자입니다. 앞에서부터 `조건문, 물음표(?), 조건문이 참일 경우 실행할 표현식, 콜론(:), 조건문이 거짓`일 경우 실행할 표현식이 배치된다
</div>
</details>


---