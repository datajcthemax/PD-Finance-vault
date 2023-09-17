`useState`는 [[React]]의 [[React Hook]] 중 하나로, 함수형 [[컴포넌트]]에서 [[상태(state)]]를 추가하고 관리하는 데 사용됩니다.

예시에서는 `useState`를 두 번 사용하여 `query`와 `darkMode`라는 두 개의 상태를 관리합니다.

1. **query 상태**:
```javascript
const [query, setQuery] = useState("");
```

- `useState`는 초기 상태 값을 인수로 받습니다. 여기서는 빈 문자열(`""`)로 `query` 상태를 초기화합니다.
- `useState`는 현재 상태값과 해당 상태를 업데이트하는 함수의 배열을 반환합니다. 이 배열의 첫 번째 원소는 상태 값이고, 두 번째 원소는 상태를 업데이트하는 함수입니다.
- `query`는 상태 값이며, `setQuery`는 상태를 업데이트하는 함수입니다.

2. **darkMode 상태**:
```javascript
const [darkMode, setDarkMode] = useState();
```

- 여기서 `useState`에 초기값을 전달하지 않았기 때문에, `darkMode`의 초기값은 `undefined`입니다.
- `darkMode`는 상태 값이며, `setDarkMode`는 상태를 업데이트하는 함수입니다.

예시에서 제공된 `handleSearch` 함수는 `setQuery`를 사용하여 `query` 상태를 업데이트합니다. 이 함수가 호출되면 전달된 `searchQuery` 값으로 `query` 상태가 업데이트됩니다.

```javascript
const handleSearch = (searchQuery) => {
    setQuery(searchQuery);
};
```

이렇게 `useState`를 사용하면 함수형 컴포넌트에서도 상태 관리를 간단하게 할 수 있습니다.