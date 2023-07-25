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
*문자열 `my_string`, `overwrite_string`과 정수 `s`가 주어집니다. 문자열 `my_string`의 인덱스 `s`부터 `overwrite_string`의 길이만큼을 문자열 `overwrite_string`으로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.*<br />

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
