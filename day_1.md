<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
</br></br>

# 프로그래머스 코딩 기초 테스트

</br>

---
## <p style="color:yellow;">1. 대문로 바꾸기</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(myString) {
    var answer ='';
    return answer;
}
```

__*[문제 설명]*__</br>
*알파벳으로 이루어진 문자열 `myString`이 주어집니다.모든 알파벳을 대문자로 변환하여 `return` 하는 `solution` 함수를 완성해 주세요.*</br>

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"></br>

```javascript
//이 함수는 solution 이라는 함수로 정의 되어있고, myString 이라는 파라미터 즉, 매개변수를 받아서 처리하는 역할을 한다
function solution(myString) {

//한번 밖에 쓰지 않을거니 answer를 let으로 변수 선언, 매개변수 myString을 toUpperCase() 메서드를 사용하여 대문자로 변경 한 후 answer 변수에 값을 저장
let answer = myString.toUpperCase();

//변경된 값을 반환
return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>메서드 `toUpperCase()`는 대문자로 변환된 호출 문자열 값을 반환합니다(값이 문자열이 아닌 경우 문자열로 변환됨)

>영어로 된 문자열은 `toUpperCase()`, `toLowerCase()` 메서드를 사용하여 각각 대문자, 소문자로 변경할 수 있다.


</div>
</details>


---

</br></br>

---
## <p style="color:yellow;">2. 소문로 바꾸기</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(myString) {
    var answer ='';
    return answer;
}
```

__*[문제 설명]*__</br>
*알파벳으로 이루어진 문자열 `myString`이 주어집니다. 모든 알파벳을 소문자로 변환하여 `return` 하는 `solution` 함수를 완성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1">

```javascript
//이 함수는 solution 이라는 함수로 정의 되어있고, myString 이라는 파라미터 즉, 매개변수를 받아서 처리하는 역할을 한다
function solution(myString) {

    //한번 밖에 쓰지 않을거니 answer를 let으로 변수 선언, 매개변수 myString을 toLowerCase() 메서드를 사용하여 대문자로 변경 한 후 answer 변수에 값을 저장
    let answer = myString.toLowerCase();

    //값을 반환
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>메서드 `toLowerCase()`는 소문자로 변환된 호출 문자열 값을 반환합니다(값이 문자열이 아닌 경우 문자열로 변환됨)

>영어로 된 문자열은 `toUpperCase()`, `toLowerCase()` 메서드를 사용하여 각각 대문자, 소문자로 변경할 수 있다.


</div>
</details>


---
</br></br>
---
## <p style="color:yellow;">3. 문자열을 정수로 변환</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(n_str) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__</br>
*숫자로만 이루어진 문자열 `n_str`이 주어질 때, `n_str`을 정수로 변환하여 `return`하도록 `solution` 함수를 완성해주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"></br>

```javascript
//함수 solution은 n_str이라는 매개변수를 가진 함수로 정의한다
function solution(n_str) {

    //문자열을 정수로 변환해주는 과정 number 메서드를 사용하여 메서드 안에 매개변수를 담는다.
    let answer = Number(n_str);

    //값을 반환
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`Number()`은 문자열을 숫자로 변환하는 함수

>숫자로 변환할 수 없는 값인 경우 NaN을 반환


</div>
</details>


------
</br></br>
---
## <p style="color:yellow;">4. 문자열을 정수로 변환</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(my_string, is_prefix) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__</br>
*어떤 문자열에 대해서 접두사는 특정 인덱스까지의 문자열을 의미합니다. 예를 들어, "banana"의 모든 접두사는 "b", "ba", "ban", "bana", "banan", "banana"입니다.
문자열 `my_string`과 `is_prefix`가 주어질 때, `is_prefix`가 `my_string`의 접두사라면 1을, 아니면 0을 `return` 하는 `solution` 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"></br>

```javascript
// solution이라는 함수는 my_string, is_prefix 두개의 매개변수를 받는 함수로 정의
function solution(my_string, is_prefix) {

    //answer는 0을 저장한다
    let answer = 0;

    //조건문 활용
    //startsWith 호출하여 my_string이 is_prefix로 시작한다면 answer = 1로 저장
    if (my_string.startsWith(is_prefix)) {
        answer = 1;

    //true가 아니라면 answer를 반환
    } else {
        return answer;
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`.startsWith()`는 주어진 문자열이 특정 문자열로 시작하는지 확인한다

>주어진 문자열로 시작한다면 `true`, 아니면 `false`를 반환


</div>
</details>


---
</br></br>
---
## <p style="color:yellow;">5. 문자열을 정수로 변환</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, b, flag) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__</br>
*두 정수 a, b와 boolean 변수 `flag`가 매개변수로 주어질 때, `flag`가 `true`면 a + b를 false면 a - b를 return 하는 `solution` 함수를 작성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"></br>

```javascript
//solution이라는 함수는 정수 a, b와 매개변수 flag를 받아서 처리하는 함수로 정의
function solution(a, b, flag) {
    //answer에 0을 저장
    let answer = 0;
    //flag가 'true'일 때 조건문 작성
    if (flag == true) {
        answer =  a + b;
    //flag가 'true'가 아닐 때
    } else {
        answer = a - b;
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`boolean 변수`란
어떤 프로그래밍 언어에도 존재하는 자료형, 값이 `true` 또는 `false`, 총 2개밖에 존재하지 않는 자료형, 바로 Boolean 자료형이다.

>이 변수는 `true` 또는 `false` 두 가지 값 중 하나를 가질 수 있다.


</div>
</details>


---