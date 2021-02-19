# 변수 와 상수

##  변수 선언
```javascript
let a = 22;
// 일반적인 변수 선언 방식
// 변수를 선언 할 때, 변수의 이름은 추후에도 어떤 값을 의미하는지 확인하기 쉬워야 한다.

let target; 
let target1 = undefined 
// 변수를 선언했으나 그 값은 없는 상태

let a = 1, b = 2, c = 'helllo';
// 다음과 같이 한줄에 여러개의 변수를 선언 할수 있다.

const DAYTIME = 24;
// 변경되지 않는 상수 값은 일반적으로 대문자 변수에 저장한다.
```
되도록이면 **상수**를 사용하는게 변수를 사용하는 것 보다 낫다.
절대 변경될 일이 없는 상수는 그 숫자 자체를 사용하는 것이 의도하지 않은 데이터의 변화를 피할 수 있다.

# 2. 식별자 이름
변수, 상수, 함수명을 식별자라고 한다.
- 식별자는 반드시 글자나 달러 기호`$`, 밑줄`_`로 시작해야 한다.
- 식별자에는 글자, 숫자, 달러 기호 `$`, 밑줄`_`만 쓸 수 있다.
- 유니코드 문자도 가능하다.
- 예약어는 식별자로 쓸 수 없다. (float, int)

식별자 표기법
- 카멜 케이스 (Camel Case)
`myName, firstName` 중간 단어의 구분 마다 대문자로 시작하는 형태 대문자가 중간중간 튀어나와 낙타의 혹과 같이 보인다.

- 스네이크 케이스 (snake case)
`my_name, first_name` 형식의 밑줄이 추가된 형태

어느것이 좋다고 할 수없지만 통용적으로 카멜케이스가 만ㅎ이 쓰이고 있다.

예외
 - 대문자로 시작하면 안된다. (class 예외)
 - 밑줄로 시작하는 식별자는 '내부' 변수에서만 사용한다.
 - 제이쿼리를 사용할 경우, 달러 객체는 제이쿼리 자체를 뜻한다.

## 3. 리터럴
 실제로 값을 넣어주는 것들을 리터럴이라 할 수 있다.

```js
const age = 24;
// 24가 리터럴 (literal)

const myName = "jaewon"
// "jaewon" 따옴표 안이 리터럴
```

## 4. 원시 타입과 객체

### 원시 타입
- 숫자
- 문자열
- 불리언
- null
- undefined
- 심볼 (symbol)

### 객체 타입
자바스크립트 내장 객체 타입
- Array
- Date
- RegExp
- Map과 WeakMap
- Set과 WeakSet

## 5. 숫자
자바스크립트의 숫자 : IEEE-764배정도 (double-precision) 부동소수점 숫자형식을 사용하고 이를 **더블**이라고 부른다.
- 자바스크립트 숫자 형식
```js
let count = 10;         // 숫자 리터럴 (double)
const blue = 0x0000ff;  // 16진수
const unmask = 0o0022;  // 8진수
const roomTemp = 21.5;  // 10진수
const c = 3.0e6;        // 지수(3.0 x 10^6 = 3,000,000)
cosnt e = -1.6e-19;     // 지수 (-1.6 x 10^-19 = 0.0000000000000000016)
const inf = Infinity;   // 양의 무한대
const ninf = -Infinity; // 음의 무한대
const nan = NaN;        // "숫자가 아님"
```
- 자바스크립트 내부 숫자 프로퍼티(properties)
```js
const small = Number.EPSILON;            // 1과 더 했을 때 1과 구분되는 결과를 만들 수 있는 가장 작은 값 (2.2e-16)
const bigInt = Number.MAX_SAFE_INTEGER;  // 표현할 수 있는 가장 큰 정수
const max = Number.MAX_VALUE;            // 표현할 수 있는 가장 큰 숫자
const minInt = Number.MIN_SAFE_INTEGER;  // 표현할 수 있는 가장 작은 정수
const min = Number.MIN_VALUE;            // 표현할 수 있는 가장 작은 숫자
const nInf = Number.NEGATIVE_INFINITY;   // -Infinity
const nan = Number.NaN;                  // NaN ("숫자가 아님")
const inf = Number.POSITIVE_INFINITY;    // Infinity
```
## 6. 문자열
자바스크립트 문자열은 **유니코드 텍스트**이다.
유니코드란?
> 텍스트 데이터에 관한 표준이며 사람이 사용하는 언어 대부분의 글자와 심볼에 해당하는 코드 포인트 모음 (프로그래밍에 표준적으로 사용하는 실제 문자와 1:1 대응 되는 코드 묶음)
