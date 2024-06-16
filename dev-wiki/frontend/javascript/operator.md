# Operator

## **JS 연산자**

### **산술 연산자**

기본적인 수학 연산을 수행한다.

```
    console.log(1 + 2);  // 덧셈
    console.log(4 - 2);  // 뺄셈
    console.log(3 * 2);  // 곱셈
    console.log(4 / 2);  // 나눗셈
    console.log(5 % 2);  // 나머지
```

### **할당 연산자**

변수에 값을 할당하며, 복합 할당 연산자를 통해 산술 연산과 할당을 동시에 수행할 수 있다.

```
let abc = 0;
abc += 2; // abc = abc + 2
abc -= 2; // abc = abc - 2
abc *= 2; // abc = abc * 2
abc %= 2; // abc = abc % 2
```

### **증감 연산자**

변수의 값을 1 증가시키거나 감소시킵니다. 전위(`++i`)와 후위(`i++`) 형태가 있다.

```
let abcd = 0;
abcd++;   // 후위 증가
++abcd;   // 전위 증가
abcd--;   // 후위 감소
--abcd;   // 전위 감소
```

### **논리 연산자**

`!` 연산자는 불리언 값을 반전시킵니다. 불리언이 아닌 값을 불리언으로 변환한 후 반전한다.

```
!true;      // false
!false;     // true

// Falsy 값에 대한 부정
!0;         // true
!!0;        // false
!!!0;       // true
!null;      // true
!undefined; // true
!NaN;       // true
!"";        // true

// Truethy 값에 대한 부정
!{};        // false (빈 객체)
![];        // false (빈 배열)
```

### **Nullish 병합 연산자 (`??`)**

왼쪽 피연산자가 `null` 또는 `undefined`일 때만 오른쪽 피연산자를 반환한다.

```
const n = null;
const num3 = n ?? 7;
console.log(num3); // 7
```

### **삼항 연산자 (`조건 ? 참 : 거짓`)**

조건에 따라 두 개의 표현식 중 하나를 실행한다.

```
const e = 1;
console.log(e < 2 ? "참" : "거짓");
```

### **전개 연산자 (`...`)**

배열이나 객체의 요소를 개별 요소로 확장한다.

```
const arr2 = [1, 2, 3];
const arr3 = [4, 5, 6];
const arr5 = [...arr2, ...arr3]; // [1, 2, 3, 4, 5, 6]
```

### **구조 분해 할당**

배열이나 객체의 속성을 변수로 추출한다.

```
const [a, b, c] = arr2;
console.log(a, b, c); // 1, 2, 3
```

### **선택적 체이닝 (`?.`)**

객체의 속성을 읽을 때, 해당 속성이 존재하지 않으면 `undefined`를 반환한다.

```
const user = { name: "fabric0de" };
console.log(user.address?.street); // undefined
```

### **조건문**

#### **if, else if, else 조건문**

조건에 따라 서로 다른 코드 블록을 실행한다.

```
const score = 85;

if (score >= 90) {
    console.log("A등급");
} else if (score >= 80) {
    console.log("B등급");
} else {
    console.log("C등급 이하");
}
```

#### **Switch 조건문**

표현식의 결과에 따라 여러 case 중 하나를 실행한다.

```
const grade = 'B';

switch (grade) {
    case 'A':
        console.log("우수합니다");
        break;
    case 'B':
        console.log("잘했습니다");
        break;
    case 'C':
        console.log("노력이 필요합니다");
        break;
    default:
        console.log("성적을 확인하세요");
}
```

### 반복문

#### **for 반복문**

주어진 조건이 거짓이 될 때까지 코드 블록을 반복 실행한다.

```
for (let i = 0; i < 5; i++) {
    console.log(i); // 0부터 4까지 출력
}
```

#### **for...of 반복문**

반복 가능한 객체(예: 배열)의 각 요소에 대해 실행한다.

```
const fruits = ["사과", "바나나", "체리"];
for (const fruit of fruits) {
    console.log(fruit);
}
```

#### **for...in 반복문**

객체의 모든 열거 가능한 속성에 대해 반복한다.

```
const person = {name: "김정현", age: 25, job: "개발자"};
for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

#### **while 반복문**

조건이 참인 동안 코드 블록을 반복 실행한다.

```
let count = 0;
while (count < 3) {
    console.log(count);
    count++;
}
```

#### **do...while 반복문**

코드 블록을 최소 한 번 실행한 후 조건이 참인 동안 반복한다.

```
let num = 0;
do {
  console.log(num);
  num++;
} while (num < 3);
```
