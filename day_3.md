<p align="center">
  <img src="https://file.newswire.co.kr/data/datafile2/thumb_640/2022/07/1994211446_20220703180818_7260737807.jpg">
</p>
<br /><br />

# 프로그래머스 코딩 기초 테스트

<br />

---
## <p style="color:yellow;">1. n 번째 원소까지</p>
---
**<p style="color:red; font-size:16px;">문제</p>**

```javascript
function solution(num_list, n) {
    var answer = [];
    return answer;
}
```

__*[문제 설명]*__<br />
*정수 리스트 `num_list`와 정수 `n`이 주어질 때, `num_list`의 첫 번째 원소부터 `n` 번째 원소까지의 모든 원소를 담은 리스트를 return하도록 solution 함수를 완성해주세요.*<br />

---

<details>
<summary style="color:lime; font-size:16px;">클릭하여 정답 보기</summary>
<div markdown="1"><br />

```javascript
//solution 함수는 매개변수 num_list, n 받는다
function solution(num_list, n) {
    //slice() 메서드를 사용해 num_list의 시작위차와 끝위치를 정해 그만큼만 추출하고 값은 answer에 할당하고 answer를 반환
    return answer = num_list.slice(0,n);
}
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>`slice()` 메서드는 `어떤 배열의 begin 부터 end 까지(end 미포함)에 대한 얕은 복사본을 새로운 배열 객체로 반환`합니다. 원본 배열은 바뀌지 않습니다.

>>_`*얕은 복사:` 참조(주소)값을 복사합니다. 
주소를 복사해 오기 때문에 메모리를 공유합니다. 하나의 객체(참조형)를 변경하면 두 개의 객체(참조형) 모두 값이 동일하게 변경됩니다._

>앞서 공부한 `문자열에서의 slice()` 와 `배열에서 slice()`는 기능이 다르다
여기서 사용한 `slice() 메서드는 배열 함수`


</div>
</details>


---

<br /><br />

---
## <p style="color:yellow;">2. 문자열 출력하기</p>
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
    input = [line];
}).on('close',function(){
    str = input[0];
});
```

__*[문제 설명]*__<br />
*문자열 `str`이 주어질 때, `str`을 출력하는 코드를 작성해 보세요.*

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
// 입력된 값을 저장할 빈 배열을 선언합니다.
let input = [];

// 'line' 이벤트는 사용자가 엔터(줄 바꿈)를 입력하고 데이터를 전송할 때마다 발생합니다.
// 이 때, 입력된 데이터를 배열 'input'에 저장합니다.
rl.on('line', function (line) {
    input = [line]; // 입력된 데이터를 배열로 만들어 배열 'input'에 저장합니다.
}).on('close', function () {
    // 'close' 이벤트는 사용자가 입력을 더 이상 보내지 않고, 입력 스트림이 종료될 때 발생합니다.
    // 이때, 배열 'input'에 저장된 값은 변수 'str'에 할당됩니다.
    str = input[0];
    //str 값을 출력
    console.log(str);
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**

>처음에 이렇게 간단한 건 줄 몰랐다..<br />
문제를 제대로 읽고 파악하는 능력을 좀 더 길러야겠다..

>해당 코드의 전반적인 문법은 아직 잘 모르겠지만
이해되기까지 공부를 많이 해야할 것 같다.

>`console.log()` 메서드는 `웹 콘솔에 메시지를 출력`합니다. 메시지는 (선택적 대체 값을 포함한) 단일 문자열이거나 더 많은 JavaScript 객체중 하나일 수 있습니다.

</div>
</details>


---
<br /><br />
---

## <p style="color:yellow;">3. a와 b 출력하기</p>

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
*정수 `a`와 `b`가 주어집니다. 각 수를 입력받아 입출력 예와 같은 형식으로 출력하는 코드를 작성해 보세요.*

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
    //console 를 사용하여 Number함수를 출력 출력 조건이 있으므로, 조건과 값을 연결해서 출력하기 위해 "메세지 + 값" 형식으로 사용
    console.log("a = " + Number(input[0]));
    console.log("b = " + Number(input[1]));
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>값이 `console.log()` 함수에 전달되면 `함수는 주어진 메시지와 함께 값`을 표시합니다.

>`큰 따옴표 ""` 와 `작은 따옴표 ''` 의 차이는 없으나, `역따옴표(backtick)`의 경우 `${}` 를 통해 변수를 넣어 사용할 수 있는데 이를 `템플릿 리터럴`이라 부른다




</div>
</details>


------
<br /><br />
---

## <p style="color:yellow;">4. 문자열 반복해서 출력하기</p>

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
    str = input[0];
    n = Number(input[1]);
});
```

__*[문제 설명]*__<br />
*문자열 `str`과 정수 `n`이 주어집니다.
`str`이 `n`번 반복된 문자열을 만들어 출력하는 코드를 작성해 보세요.*

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
    str = input[0];
    n = Number(input[1]);
    //repeat 메서드를 사용해 str 을 n 반큼 반복하여 출력
    console.log(str.repeat(n));
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>앞서 공부한 `repeat()` 메서드를 활용하여 적용하였다.

>`repeat()`는 주어진 문자열을 큼 할당한 수 만큼 반복


</div>
</details>


---
<br /><br />
---
## <p style="color:yellow;">5. 대소문자 바꿔서 출력하기</p>

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
*영어 알파벳으로 이루어진 문자열 `str`이 주어집니다. 각 알파벳을 대문자는 소문자로 소문자는 대문자로 변환해서 출력하는 코드를 작성해 보세요.*

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
    let str = input[0];
    let convertedStr = '';
    
    //반복문으로 각 문자를 처리 index 는 0 부터 시작하니 i가 str.lenght 보다 작을때 까지 실행
    for (let i = 0; i < str.length; i++) {
        //조건문으로 str이 소문자 a 부터 z 사이에 있으면
        if (str[i] >= 'a' && str[i] <= 'z') {
            //대문자로 변경된 str을 convertedStr에 추가
            convertedStr += str[i].toUpperCase();
        // str이 대문자 A 부터 Z 사이에 있으면
        } else if (str[i] >= 'A' && str[i] <= 'Z') {
            // 소문자로 변경된 str을 convertedStr에 추가
            convertedStr += str[i].toLowerCase();
        } else {
            convertedStr += str[i];
        }
    }
    console.log(convertedStr);
});
```
**<span style="font-size:20px; color:tomato">🧐 공부한 것 정리</span>**
>`+=` 연산자는 `변수의 현재 값과 우변의 값을 더하여 그 결과를 변수에 다시 할당`하는 역할을 합니다.
</div>
</details>


---