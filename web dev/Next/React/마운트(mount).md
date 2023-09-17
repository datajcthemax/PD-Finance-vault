"마운트(mount)"는 [[React]]에서 [[컴포넌트]]가 [[DOM(Document Object Model)]]에 처음 생성되어 삽입될 때를 나타내는 용어입니다. 마운트는 컴포넌트의 생명주기에서 중요한 단계 중 하나입니다.

React 컴포넌트의 생명주기에는 크게 세 가지 주요 단계가 있습니다:
1. **마운트(Mounting)**: 컴포넌트가 처음 DOM에 생성되고 삽입되는 단계입니다.
2. **업데이트(Updating)**: 컴포넌트의 [[상태(state)]]나 [[속성(props)]]이 변경될 때 발생하는 단계로, 컴포넌트가 재렌더링됩니다.
3. **언마운트(Unmounting)**: 컴포넌트가 DOM에서 제거되는 단계입니다.

마운트에 관련된 주요 생명주기 메서드들은:
- 클래스 컴포넌트에서: `constructor()`, `static getDerivedStateFromProps()`, `render()`, 그리고 `componentDidMount()`
- 함수형 컴포넌트에서: `useEffect` 훅 (빈 의존성 배열 `[]`을 사용하여 마운트 시만 실행되게 할 수 있습니다.)

예를 들어, 데이터를 불러오는 작업은 종종 컴포넌트가 마운트될 때 수행됩니다. 클래스 컴포넌트에서는 `componentDidMount` 메서드 내에서, 함수형 컴포넌트에서는 `useEffect` 훅 내에서 이러한 작업을 수행할 수 있습니다.