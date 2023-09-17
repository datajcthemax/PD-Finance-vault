메서드(method)는 객체 지향 프로그래밍에서 중요한 개념 중 하나로, 객체의 특정 동작이나 기능을 나타내는 함수입니다. 메서드는 해당 객체의 [[상태(state)]] 또는 행동(behavior)에 액세스하거나 수정하는 데 사용됩니다.

### 메서드의 특징:

1. **객체와 연결**: 메서드는 특정 객체와 연관되어 있습니다. 이 객체는 메서드를 호출하는 대상이 됩니다.
2. **상태 액세스**: 메서드는 객체의 내부 상태에 액세스할 수 있습니다.
3. **재사용성**: 메서드를 사용하면 코드의 재사용성이 높아집니다. 동일한 코드나 로직을 여러 번 작성하는 대신 메서드를 정의하고 필요한 곳에서 호출할 수 있습니다.

### JavaScript에서의 메서드:

JavaScript는 프로토타입 기반의 객체 지향 언어로, 객체의 메서드를 정의하고 호출하는 방법을 제공합니다.

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
    fullName: function() {
        return this.firstName + " " + this.lastName;
    }
};

console.log(person.fullName()); // 출력: John Doe
```

위의 예제에서 `person` 객체에는 `fullName`이라는 메서드가 있습니다. 이 메서드는 객체의 `firstName`과 `lastName` 속성을 사용하여 전체 이름을 반환합니다.

### React에서의 메서드:

React의 클래스 컴포넌트에서도 메서드를 정의하여 컴포넌트의 동작을 구현할 수 있습니다.

```javascript
import React, { Component } from 'react';

class MyComponent extends Component {
    state = {
        count: 0
    };

    handleIncrement = () => {
        this.setState({ count: this.state.count + 1 });
    };

    render() {
        return (
            <div>
                <p>Count: {this.state.count}</p>
                <button onClick={this.handleIncrement}>Increment</button>
            </div>
        );
    }
}

export default MyComponent;
```

위의 예제에서 `handleIncrement`는 `MyComponent` 클래스의 메서드로, 버튼 클릭 시 호출되어 상태의 `count` 값을 증가시킵니다.