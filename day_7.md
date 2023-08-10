<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. 주사위 게임 2</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, b, c) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*1부터 6까지 숫자가 적힌 주사위가 세 개 있습니다. 세 주사위를 굴렸을 때 나온 숫자를 각각 `a`, `b`, `c`라고 했을 때 얻는 점수는 다음과 같습니다.*
<br />

+ 세 숫자가 모두 다르다면 `a` + `b` + `c` 점을 얻습니다.<br />
+ 세 숫자 중 어느 두 숫자는 같고 나머지 다른 숫자는 다르다면 (`a` + `b` `c`) × (`a`<sup>2</sup> + `b`<sup>2</sup> + `c`<sup>2</sup> )점을 얻습니다.<br />
+ 세 숫자가 모두 같다면 (`a` + `b` + `c`) × (`a`<sup>2</sup> + `b`<sup>2</sup> + `c`<sup>2</sup> ) × (`a`<sup>3</sup> + `b`<sup>3</sup> + `c`<sup>3</sup> )점을 얻습니다.<br />

*세 정수 `a`, `b`, `c`가 매개변수로 주어질 때, 얻는 점수를 return 하는 solution 함수를 작성해 주세요.*<br />


---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(a, b, c) {
    let answer = 0;
    // 조건문으로 문제의 경우 작성
    if (a === b && b === c) {
        answer = (a + b + c) * (a ** 2 + b ** 2 + c ** 2) * (a ** 3 + b ** 3 + c ** 3);
    } else if (a === b || a === c || b === c) {
        answer = (a + b + c) * (a ** 2 + b ** 2 + c ** 2);
    } else {
        answer = a + b + c;
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>조건문에서 순서에 따라 값이 달라지는 걸 알았다
조건문의 순서를 어떻게 짤지 논리적으로 생각해야한다

</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 원소들의 곱과 합</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(num_list) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*정수가 담긴 리스트 `num_list`가 주어질 때, 모든 원소들의 곱이 모든 원소들의 합의 제곱보다 작으면 1을 크면 0을 return하도록 solution 함수를 완성해주세요.*


---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1">

```javascript
function solution(num_list) {
    let answer = 0;
    let multiply = 1; // forEach 로 곱한 뒤 대입해야해서 값을 1로 설정 
    let sumSquared = 0;
    
    num_list.forEach(num_list => multiply *= num_list); // 모든 배열의 곱
    num_list.forEach(num_list => sumSquared += num_list); // 모든 배열의 합
    
    sumSquared = Math.pow(sumSquared, 2); // sumSquared 변수의 제곱
    
    if (multiply < sumSquared) {
        answer = 1;
    } else {
        answer = 0;
    }
    
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`forEach()` 메서드는 주어진 함수를 배열 요소 각각에 대해 실행합니다<br />
`Math.pow()` 함수는 base^exponent 처럼 base 에 exponent를 제곱한 값을 반환합니다.

</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. 이어 붙인 수 </p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(num_list) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*정수가 담긴 리스트 `num_list`가 주어집니다. `num_list`의 홀수만 순서대로 이어 붙인 수와 짝수만 순서대로 이어 붙인 수의 합을 return하도록 solution 함수를 완성해주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(num_list) {

    let even = num_list.filter(number => number % 2 === 0).join('');
    let odd = num_list.filter(number => number % 2 === 1).join('');

    let answer = Number(even) + Number(odd); 
    
    return answer;
}

```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`filter()` 메서드는 주어진 함수의 테스트를 통과하는 모든 요소를 모아 새로운 배열로 반환합니다.

</div>
</details>


------
<br /><br />
---

## <p style="color:yellow;">4. 마지막 두 원소</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(num_list) {
    var answer = [];
    return answer;
}
```

__*[문제 설명]*__<br />
*정수 리스트 `num_list`가 주어질 때, 마지막 원소가 그전 원소보다 크면 마지막 원소에서 그전 원소를 뺀 값을 마지막 원소가 그전 원소보다 크지 않다면 마지막 원소를 두 배한 값을 추가하여 return하도록 solution 함수를 완성해주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(num_list) {
    var answer = [];
    
    let len = num_list.length;
    
    if (num_list[len-1] > num_list[len-2]) {
        num_list.push(num_list[len-1] - num_list[len-2]);
        answer = num_list;
    } else {
        num_list.push(num_list[len-1] * 2);
        answer = num_list;
    }
    return answer;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`push()` 메서드는 배열의 끝에 하나 이상의 요소를 추가하고, 배열의 새로운 길이를 반환합니다.
</div>
</details>


---
<br /><br />
---
## <p style="color:yellow;">5. 수 조작하기 1</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(a, d, included) {
    var answer = 0;
    return answer;
}
```

__*[문제 설명]*__<br />
*정수 `n`과 문자열 `control`이 주어집니다. `control`은 "w", "a", "s", "d"의 4개의 문자로 이루어져 있으며, `control`의 앞에서부터 순서대로 문자에 따라 `n`의 값을 바꿉니다.*<br />

* *"w" : n이 1 커집니다.*
* *"s" : n이 1 작아집니다.*
* *"d" : n이 10 커집니다.*
* *"a" : n이 10 작아집니다.*
  
*위 규칙에 따라 `n`을 바꿨을 때 가장 마지막에 나오는 `n`의 값을 return 하는 solution 함수를 완성해 주세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
function solution(n, control) {
    for (let i = 0; i < control.length; i++) {
        switch(control[i]) {
            case "w" :
                n += 1;
                break;
            case "s" :
                n -= 1;
                break;
            case "d" :
                n += 10;
                break;
            case "a" :
                n -= 10;
                break;
        }
    }
    return n;
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>switch 문은 특정 값에 대한 여러 가지 경우(case)에 따라 다른 코드 블록을 실행하는 조건문입니다. <br /> 이는 일련의 값들 중 하나가 변수나 표현식으로 주어졌을 때, 해당 값이 어떤 경우(case)에 해당하는지 판별하고 해당하는 코드 블록을 실행합니다.

>해당 조건에 맞는 case를 구분해서 수행하는 제어문입니다.
<br />
```
switch문

let 변수 = 초기값;

switch (조건을 체크할 변수) {
    case 값1: 코드1;
        //조건을 체크할 변수가 값1을 가지면 실행
    break;
    case 값2: 코드2;
        //조건을 체크할 변수가 값2을 가지면 실행
    break;
    case 값3: 코드3;
        //조건을 체크할 변수가 값3을 가지면 실행
    break;
    case 값4: 코드4;
    break;
default;
    //해당되는 값을 가지고 있지 않을 경우 실행
}
```
</div>
</details>


---