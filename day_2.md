<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. rny_string</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(rny_string) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*`m`과 `rn`이 모양이 비슷하게 생긴 점을 활용해 문자열에 장난을 하려고 합니다. <br />문자열 `rny_string`이 주어질 때, `rny_string`의 모든 `m`을 `rn`으로 바꾼 문자열을 `return` 하는 `solution` 함수를 작성해 주세요.*<br />

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
//solution은 rny_string 라는 변수를 가진 함수로 정의
function solution(rny_string) {
    
    //replaceAll 메서드를 사용해 변수 rny_string의 모든 'm' 이라는 문자열을 'rn'으로 변환하고 answer에 저장
    let answer = rny_string.replaceAll( 'm' , 'rn' )
    
//answer를 반환
return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`replaceAll()` 메서드는 pattern의 모든 일치 항목이 replacement로 대체된 새 문자열을 반환합니다.<br /> pattern은 문자열 또는 RegExp일 수 있으며 replacement는 각 일치 항목에 대해 호출되는 문자열 또는 함수일 수 있습니다. <br />원래 문자열은 변경되지 않습니다.

>문법
`string.replaceAll(pattern, replacement)`

>처음에 `replace` 사용했지만 'mm'처럼 연속되는 문자열에 대한 반환을 한번밖에 못해서 결국 검색을 통해 `replaceAll`이라는 메서드가 있다는 것을 알게 되었다.


</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 공배수</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(number, n, m) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*정수 `number`와 `n, m`이 주어집니다. `number`가 `n`의 배수이면서 `m`의 배수이면 `1`을 아니라면 `0`을 `return`하도록 `solution` 함수를 완성해주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1">

```javascript
//함수 solution은 정수 'number, n, m' 변수를 받는다
function solution(number, n, m) {
    
    //조건문으로 number를 n 과 m으로 나누었을 때 두 조건이 모두 나머지가 0이라면
    if (number % n === 0 && number % m === 0) {
        // answer = 0로 반환
        return answer = 1;
    } else {
        //나머지가 1이 아니라면 1을 반환
        return answer = 0;
    }
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`||`과 `&&` 연산자를 정확하게 몰라 ||로 풀었는데 찾아보니 잘못된 풀이였다

>`||연산자`는 둘중 하나가 참이라면 true를 반환하고<br />
`&&연산자`는 모든 조건이 참이여야 true를 반환한다

>또 문제를 반대로 나머지가 1이라면 0 그렇지 않다면 1을 출력하도록 반대로 작성했었다


</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. 문자열의 앞의 n글자</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(my_string, n) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*문자열 `my_string`과 정수 `n`이 매개변수로 주어질 때, `my_string`의 앞의 `n`글자로 이루어진 문자열을 return 하는 solution 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
//함수 solution은 문자열 my_string, 정수 n을 매개변수로 받는다
function solution(my_string, n) {
    //substring 메서드를 사용해 종료 인덱스를 n으로 할당
    let answer = my_string.substring(0,n);
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`substring()` 메서드는 시작 인덱스로 부터 종료 인덱스 전까지의 문자열을 반환하는 메서드

>`substring` 메서드
  >>문법: `string.substring(startIndex, length)`

>그 외 `substr`, `slice` 도 함께 알아보았다
>>`substr` 메서드는 `substring` 메서드와 비슷하지만 `startIndex` 가 음수라면 `역순으로 카운트`를 하고 반면 `substring` 는 `음수는 0으로 취급`한다<br /><br />
`slice` 메서드는 문자열의 뒤에서 부터 카운트 한다




</div>
</details>


------
<br /><br />
---
## <p style="color:yellow;">4. 부분 문자열인지 확인하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(my_string, target) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*부분 문자열이란 문자열에서 연속된 일부분에 해당하는 문자열을 의미합니다. <br />예를 들어, 문자열 "ana", "ban", "anana", "banana", "n"는 모두 문자열 "banana"의 부분 문자열이지만, "aaa", "bnana", "wxyz"는 모두 "banana"의 부분 문자열이 아닙니다.*

문자열 `my_string`과 `target`이 매개변수로 주어질 때, `target`이 문자열 `my_string`의 부분 문자열이라면 1을, 아니라면 0을 return 하는 solution 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
//solution 은 my_string, target을 매개변수로 받는다
function solution(my_string, target) {
    //조건문을 사용해서 my_string 이 target 을 포함하면
    if (my_string.includes(target)) {
        //answer 는 1을 반환
        return answer = 1;
    //target 을 포함하지 않는다면,
    } else {
        //answer 0을 반환
        return answer = 0;
    }
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`.includes()`는  메서드는 `하나의 문자열이 다른 문자열에 포함되어 있는지를 판별`하고, 결과를 true 또는 false 로 반환합니다. 검색 시 대소문자를 구분합니다.


</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">5. 문자열 곱하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(my_string, k) {
    var answer = '';
    return answer;
}
```

__*[문제 설명]*__<br />
*문자열 `my_string`과 정수 `k`가 주어질 때, `my_string`을 `k`번 반복한 문자열을 return 하는 solution 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
//solution 함수는 my_srting, k 매개변수를 받는다
function solution(my_string, k) {
    //my_string 문자열에 k를 곱한 값을 answer에 저장
    let answer = my_string.repeat(k);
    //answer 를 반환
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`repeat()` 메서드는 문자열을 `주어진 횟수만큼 반복`해 붙인 새로운 문자열을 반환합니다.

</div>
</details>


---