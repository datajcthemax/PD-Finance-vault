JSX는 [[JavaScript]] [[XML]]의 약어로, JavaScript 코드 안에서 XML 또는 HTML과 유사한 문법을 사용하여 UI 요소를 정의하는 확장 문법입니다. JSX는 주로 React와 같은 라이브러리 및 프레임워크에서 사용되며, 사용자 인터페이스를 빌드하기 위한 강력한 도구로 사용됩니다.

JSX의 주요 특징과 사용법은 다음과 같습니다:

1. **JavaScript 확장**: JSX는 JavaScript를 확장한 문법으로, JavaScript 코드 내에서 사용됩니다. 따라서 JavaScript 변수와 함수를 JSX 내에서 직접 참조하고 사용할 수 있습니다.

2. **UI 요소 정의**: JSX를 사용하여 UI 요소(예: 버튼, 폼, 텍스트, 이미지)를 HTML과 유사한 방식으로 정의할 수 있습니다. JSX에서는 각 요소를 태그와 속성을 사용하여 표현합니다.

3. **컴포넌트**: JSX에서 정의된 UI 요소는 컴포넌트로 간주됩니다. 컴포넌트는 재사용 가능한 UI 조각을 나타내며, 더 큰 애플리케이션에서 조립하여 사용할 수 있습니다.

4. **표현식 삽입**: JSX 내에서 중괄호 `{}`를 사용하여 JavaScript 표현식을 삽입할 수 있습니다. 이를 통해 동적 데이터를 UI에 표시하거나 조작할 수 있습니다.

5. **이벤트 처리**: JSX에서는 이벤트 핸들러를 속성으로 지정하여 사용자 상호 작용을 처리할 수 있습니다. 예를 들어, 클릭 이벤트에 대한 핸들러를 지정할 수 있습니다.

6. **조건문과 반복문**: JSX 내에서 JavaScript의 조건문(예: `if` 문)과 반복문(예: `for` 루프)을 사용하여 동적 UI를 생성할 수 있습니다.

예를 들어, 다음은 JSX를 사용하여 간단한 React 컴포넌트를 정의하는 예제입니다:

```jsx
import React from 'react';

function MyComponent(props) {
  return (
    <div>
      <h1>Hello, {props.name}!</h1>
      <p>This is a simple React component.</p>
      <button onClick={props.onClick}>Click me</button>
    </div>
  );
}
```

위의 코드에서 `<h1>` 태그, `<p>` 태그, 그리고 `<button>` 태그는 JSX를 사용하여 정의되었습니다. 중괄호 `{}` 내에 있는 `props.name` 및 `props.onClick`는 JavaScript 표현식을 삽입한 예입니다.

JSX는 번들링 도구(Bundler)를 사용하여 브라우저에서 실행 가능한 JavaScript 코드로 컴파일됩니다. 이렇게 변환된 JSX 코드는 웹 애플리케이션에서 사용되며, 사용자 인터페이스를 생성하고 동적으로 조작하는 데 사용됩니다.