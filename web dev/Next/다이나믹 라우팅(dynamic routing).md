Next.js는 프레임워크의 일부로 다이나믹 라우팅(dynamic routing)을 제공합니다. 다이나믹 라우팅은 라우트의 일부로 변수를 사용하여 동적으로 페이지를 생성하는 방법을 의미합니다.

다이나믹 라우팅의 주요 특징은 다음과 같습니다:

1. **앱기반**: Next.js는 `app` 디렉토리 내의 파일 구조를 기반으로 자동으로 라우트를 생성합니다.
2. **브래킷 문법**: 다이나믹 라우트를 정의할 때, 브래킷(`[]`)을 사용합니다.

### 다이나믹 라우팅 사용 방법:

1. `app` 디렉토리 내에 다이나믹 라우트를 정의하려면 브래킷으로 파일 또는 디렉토리 이름을 둘러싸야 합니다.
   - 예: `app/[company]/page.js` 파일은 `/AAPL`, `/META` 등의 라우트를 생성합니다.
   - 여기서 `company`는 동적 세그먼트로, 실제 라우트에서 해당 부분의 값을 가져올 수 있습니다.

다이나믹 라우팅은 Next.js의 강력한 기능 중 하나로, 동적인 웹 애플리케이션을 구축하는 데 있어 중요한 역할을 합니다.