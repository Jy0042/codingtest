<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. n 특수문자 출력하기</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

rl.on('close', function () {
    
});
```

__*[문제 설명]*__<br />
*다음과 같이 출력하도록 코드를 작성해 주세요.*<br />

__*[출력 예시]*__<br />
```
!@#$%^&*(\'"<>?:;
```

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

rl.on('close', function () {
    //console.log로 특수문자를 출력 주어진 특수문자에 ', " 이 사용되고 있어 `` 안에 문자열을 입력
    console.log(`!@#$%^&*(\\'"<>?:;`);
    //'," 사용하고 있어 \로 우선 처리하고 전체 문자를 ""로 감싸주었다
    //console.log("!@#$%^&*(\\'\"<>?:;");
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`` 로 감싸면 문자열로 출력된다

>\는 출력하기 위해서는 2번 사용해야한다


</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 덧셈식 출력하기</p>
---

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    console.log(Number(input[0]) + Number(input[1]));
});
```

__*[문제 설명]*__<br />
*두 정수 `a`, `b`가 주어질 때 다음과 같은 형태의 계산식을 출력하는 코드를 작성해 보세요.*
```
a + b = c
```
---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1">

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
    
}).on('close', function () {
    // 두개의 input을 더한 값을 변수 i에 저장
    const i = Number(input[0]) + Number(input[1]);
    //input의 값이 출력 되어야해 "" 를 사용해 + 를 사용해 식과 연결
    console.log(Number(input[0])+"" + " + " + Number(input[1])+ " = " + i);
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>너무 하드코딩 한 거 같아 더 좋은 방법이 있을 거 같아서 찾아봤다<br />~~나도 조금만 더 생각하면 충분히 할 수 있던 방식이 였는데 조금 더 사고력을 기를 수 있게 노력해야겠다...~~

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    //한번 값이 할당되면 변하지 않는 상수 이므로 const로 선언
    const a = Number(input[0]);
    const b = Number(input[1]);
    const sum = a + b;
    // ${} 이라는 템플릿 리터럴 사용해 문자열 중간에 변수 삽입
    console.log(`${a} + ${b} = ${sum}`);
});
```

>`const` 는 상수로 선언할때 사용!

>`ES6 이전`에는 `템플릿 문자열`이라고 부르던 것을 <br />`ES6 에서` `템플릿 리터럴`이라 부르게 되었다.

>`${}` 를 사용하면 `문자열 중간에 변수, 표현식 등을 삽입`할 수 있습니다. <br /> `${}` 내부에는 유효한 JavaScript 표현식을 작성할 수 있으며, 이 `표현식의 결과가 해당 위치에 문자열로 포함`됩니다.

</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. 문자열 붙여서 출력하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str1 = input[0];
    str2 = input[1];
});
```

__*[문제 설명]*__<br />
*두 개의 문자열 `str1`, `str2`가 공백으로 구분되어 입력으로 주어집니다.
입출력 예와 같이 `str1`과 `str2`을 이어서 출력하는 코드를 작성해 보세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str1 = input[0];
    str2 = input[1];
    
    //+연산자를 사용하여 문자열을 합쳐줄수있다
    console.log(str1 + str2);
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>다른 방법으로 풀 수 있는 지 찾아보았다

>`join()` 메서드는 `배열의 모든 요소를 연결`해 `하나의 문자열`로 만듭니다.

>`join()` 메서드를 사용한 풀이 ~~(이게 좀 더 개발자스러운 것 같다..)~~

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {

    //input은 값을 나눠서 받기에 배열 형식
    //join 메서드를 사용해 배열을 연결
    console.log(input.join(''));
});
```




</div>
</details>


------
<br /><br />
---

## <p style="color:yellow;">4. 문자열 돌리기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = [line];
}).on('close',function(){
    str = input[0];
});
```

__*[문제 설명]*__<br />
*문자열 `str`이 주어집니다.
문자열을 시계방향으로 90도 돌려서 아래 입출력 예와 같이 출력하는 코드를 작성해 보세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = [line];
}).on('close',function(){
    // str은 input 으로 값을 할당받는 상수 이므로 const로 선언
    const str = input[0];
    // 반복문으로 str의 문자열의 길이를 만큼 실행되게 작성
    for (let i = 0; i < str.length; i++) {
        // str의 각 문자열 출력
        console.log(str[i]);
    }
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`for` 문이 `한 줄의 코드 블록`을 가지는 경우 `중괄호를 생략` 할 수 있다.

>`ES6` 문법으로 `for문` 을 아래처럼 작성할 수 있다.
```javascript
for (let i of str) console.log(i)
```

>`ES6` 문법을 사용하여 `javascript` 코드를 작성하면 정말 간편하게 작성할 수 있을 거 같다


</div>
</details>


---
<br /><br />
---
## <p style="color:yellow;">5. 홀짝 구분하기</p>

**<p style="color:red; font-size:16px;">문제</p>**

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    n = Number(input[0]);
});
```

__*[문제 설명]*__<br />
*자연수 `n`이 입력으로 주어졌을 때 만약 `n`이 짝수이면 "`n` is even"을, 홀수이면 "`n` is odd"를 출력하는 코드를 작성해 보세요.*

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    // n은 input으로 할당 받으면 상수 이므로 const로 선언
    const n = Number(input[0]);
    // 조건문으로 n을 2로 나눈 값이 0 이라면
    if (n % 2 === 0 ) {
        //"n is even" 을 출력
        console.log(`${n} is even`);
        // 값이 1 이라면
    } else if (n % 2 === 1) {
         //"n is odd" 을 출력
        console.log(`${n} is odd`);
    } 
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>이번 문제는 비교적 쉽고 간단하게 풀었다

>`ES6` 문법을 사용해 출력해보았다
</div>
</details>


---