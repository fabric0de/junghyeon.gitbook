# Function

### **JS 함수 선언 방법**

JavaScript에서 함수는 크게 선언문(Function Declaration) 방식과 표현식(Function Expression) 방식으로 정의한다.

#### **함수 선언문 (Function Declaration)**

함수 선언문은 `function` 키워드를 사용하여 이름이 지정된 함수를 정의한다.\
함수 선언문은 호이스팅 되므로, 선언 전에 호출할 수 있다.

> 호이스팅(Hoisting)\
> 호이스팅(Hoisting)은 JavaScript에서 변수와 함수 선언을 코드의 최상단으로 끌어올리는 동작이다.\
> 이로 인해 코드의 어느 위치에서든지 함수를 호출할 수 있다.

```
// 함수 선언문
function sum(a, b) {
    return a + b;
}

console.log(sum(2, 3)); // 5
```

#### **함수 표현식 (Function Expression)**

함수 표현식은 `function` 키워드를 사용하여 함수를 정의하고, 이를 변수에 할당한다.\
익명 함수(Anonymous Function) 또는 명명된 함수(Named Function)를 사용할 수 있다.

```
// 익명 함수 표현식
const add = function(a, b) {
    return a + b;
};

// 명명된 함수 표현식
const subtract = function sub(a, b) {
    return a - b;
};

console.log(add(5, 3)); // 8
console.log(subtract(10, 5)); // 5
```

### **함수 선언문 VS 함수 표현식**

#### **함수 선언문**

**장점**

1. 코드의 어느 위치에서든지 함수를 호출할 수 있는 유연성을 제공한다.
2. 이로 인해 코드 구조를 더 자유롭게 할 수 있게 해준다.
3. 함수의 이름이 디버깅 스택에 나타나므로 디버깅이 더 쉽다.

**단점**

1. 호이스팅으로 인해 코드의 실행 흐름이 직관적이지 않을 수 있다.
2. 코드의 하단에 정의된 함수를 상단에서 호출하는 것이 가능하므로, 코드를 읽는 흐름을 방해할 수 있다.

#### **함수 표현식**

**장점**

1. 조건부로 함수를 정의할 수 있어서 더 동적인 함수 생성이 가능하다. (함수를 변수에 할당하기 전에 특정 조건을 체크할 수 있다.)
2. IIFE(Immediately Invoked Function Expression) 패턴을 사용하여 스코프를 제한하고, 즉시 실행되는 함수를 만들 수 있다.
3. 익명 함수를 사용할 수 있어서, 빠르고 간단한 함수를 필요로 할 때 유용하다.

**단점**

1. 함수가 선언된 후에만 호출할 수 있으므로, 코드 구성에 더 주의가 필요하다.
2. 익명 함수는 스택 추적에서 이름이 나타나지 않아 디버깅이 더 어려울 수 있다.
