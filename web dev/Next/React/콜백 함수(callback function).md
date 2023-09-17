콜백 함수(callback function)는 다른 함수에 인자로 전달되는 함수를 의미합니다. 전달된 콜백 함수는 호스팅 함수(hosting function) 내에서 실행되거나 나중에 어떤 이벤트나 조건에 따라 실행됩니다.

콜백 함수의 주요 특징과 사용 사례는 다음과 같습니다:

1. **비동기 작업**: [[JavaScript]]에서 비동기 작업 (예: 타이머, [[HTTP(하이퍼텍스트 전송 프로토콜, Hypertext Transfer Protocol)]] 요청, 이벤트 리스너)을 처리할 때 콜백 함수가 널리 사용됩니다.
2. **함수의 완료 시점**: 콜백 함수는 호스팅 함수의 작업이 완료된 후에 실행될 수 있습니다. 이렇게 하면 함수의 실행 후 추가 작업을 수행할 수 있습니다.
3. **반복 작업**: 배열의 `map`, `filter`, `reduce`와 같은 [[메서드(Method)]]에서 콜백 함수를 사용하여 각 요소에 대한 반복 작업을 수행할 수 있습니다.
4. **사용자 정의 동작**: 라이브러리나 프레임워크가 제공하는 기능에 사용자 정의 동작을 추가하려면 콜백 함수를 사용할 수 있습니다.

### 예제:

1. **타이머를 사용한 콜백**:
```javascript
setTimeout(function() {
    console.log("3초 후에 출력됩니다.");
}, 3000);
```

2. **배열의 map 메서드를 사용한 콜백**:
```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(function(number) {
    return number * 2;
});
console.log(doubled); // [2, 4, 6, 8]
```

3. **React에서의 콜백**:
React에서는 부모 컴포넌트에서 자식 컴포넌트로 콜백 함수를 props로 전달하여 자식 컴포넌트에서 어떤 동작이 발생했을 때 부모 컴포넌트에 알릴 수 있습니다.
```jsx
function ParentComponent() {
    const handleChildClick = () => {
        console.log("자식 컴포넌트에서 클릭됨!");
    };

    return <ChildComponent onClick={handleChildClick} />;
}

function ChildComponent(props) {
    return <button onClick={props.onClick}>클릭하세요!</button>;
}
```

콜백 함수는 JavaScript의 중요한 패턴 중 하나이며, 비동기 프로그래밍, 이벤트 처리, 함수형 프로그래밍 등 다양한 상황에서 사용됩니다.