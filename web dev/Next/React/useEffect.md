`useEffect`는 [[React Hook]] 중 하나로, 함수형 [[컴포넌트]] 내에서 부수 효과(side effects)를 수행할 때 사용합니다. 부수 효과는 데이터 가져오기, 구독 설정하기, 수동으로 React 컴포넌트의 [[DOM(Document Object Model)]]을 수정하는 것과 같은 작업을 포함합니다.

메인페이지 예제를 기반으로 `useEffect`의 기능과 사용법을 설명하겠습니다:

1. **첫 번째 `useEffect`**:
```javascript
useEffect(() => {
    const storedDarkMode = localStorage.getItem("darkMode");
    if (storedDarkMode) {
        setDarkMode(storedDarkMode === "true");
    }
}, []);
```
- 이 `useEffect`는 컴포넌트가 처음 [[마운트(mount)]]될 때만 실행됩니다. (의존성 배열이 빈 배열 `[]`이므로)
- 로컬 스토리지에서 `"darkMode"` 키의 값을 가져와서, 그 값이 `"true"`라면 `setDarkMode` 함수를 사용하여 `darkMode` 상태를 `true`로 설정합니다.
- 이렇게 하면 사용자의 다크 모드 선호도를 기억하고 페이지를 다시 로드할 때 해당 설정을 적용할 수 있습니다.

2. **두 번째 `useEffect`**:
```javascript
useEffect(() => {
    if (darkMode) {
        document.body.classList.add('dark');
    } else {
        document.body.classList.remove('dark');
    }
}, [darkMode]);
```
- 이 `useEffect`는 `darkMode` 상태가 변경될 때마다 실행됩니다.
- `darkMode` 값에 따라 웹 페이지의 body에 "dark" 클래스를 추가하거나 제거합니다. 이 클래스를 통해 다크 모드와 라이트 모드의 스타일을 CSS에서 적용할 수 있습니다.

`useEffect`의 핵심 개념은:
- 첫 번째 인자로 전달된 함수는 컴포넌트가 렌더링된 후에 실행됩니다.
- 두 번째 인자는 선택적인 의존성 배열입니다. 배열에 특정 상태나 속성을 포함시키면 해당 상태나 속성이 변경될 때만 `useEffect` 내의 함수가 실행됩니다. 배열이 비어 있으면 `useEffect` 내의 함수는 컴포넌트가 처음 마운트될 때만 실행됩니다.

이렇게 `useEffect`를 사용하면 함수형 컴포넌트에서도 생명주기 메서드와 유사한 기능을 수행할 수 있습니다.