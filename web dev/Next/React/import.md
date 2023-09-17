React에서 `import` 문은 파일에 의존성이나 모듈을 가져오는 데 사용됩니다. 이것은 ES6 모듈 시스템의 일부로, React 프로젝트에서 [[컴포넌트]]나 라이브러리를 가져올 때 주로 사용됩니다.

예시:

1. **React와 ReactDOM 불러오기**:
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
```

2. **다른 파일에 있는 컴포넌트 불러오기**:
```javascript
import MyComponent from './MyComponent';
```

3. **라이브러리 또는 패키지 불러오기**:
```javascript
import axios from 'axios';
```

이렇게 `import` 문을 사용하면 필요한 모듈이나 컴포넌트, 라이브러리를 현재 파일에 가져와 사용할 수 있습니다.