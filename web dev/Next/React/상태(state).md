[[React]]에서 "상태(state)"는 [[컴포넌트]]의 [[데이터(Data)]]를 나타내며, 시간에 따라 변경될 수 있습니다. 상태는 사용자의 인터랙션, [[API(Application Programming Interface)]]
호출의 응답 등으로 인해 변경될 수 있으며, 상태가 변경될 때마다 컴포넌트는 다시 렌더링됩니다.

상태의 주요 특징은 다음과 같습니다:

1. **변경 가능성**: 상태는 변할 수 있습니다. 상태가 변경되면 해당 컴포넌트 (및 필요한 하위 컴포넌트)가 다시 렌더링됩니다.
2. **컴포넌트 내부에서 관리**: 상태는 컴포넌트 내에서 관리되며, 각 컴포넌트는 자체 상태를 가질 수 있습니다.
3. **초기화**: 컴포넌트의 초기 상태는 컴포넌트가 마운트될 때 설정됩니다.
4. **변경 [[메서드(Method)]]**: 상태를 직접 수정하는 것은 권장되지 않습니다. 대신, 클래스 컴포넌트에서는 `setState` 메서드를, 함수형 컴포넌트에서는 [[useState]] 훅을 사용하여 상태를 변경합니다.

### 예제:


1. **함수형 컴포넌트에서의 상태**:
```javascript
import React, { useState } from 'react';

function MyComponent() {
    const [count, setCount] = useState(0);

    const handleIncrement = () => {
        setCount(count + 1);
    };

    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={handleIncrement}>Increment</button>
        </div>
    );
}

export default MyComponent;
```

위의 예제에서, `count`는 컴포넌트의 상태를 나타내며, 버튼을 클릭할 때마다 증가합니다. 상태가 변경될 때마다 컴포넌트는 해당 부분을 다시 렌더링합니다.