쿠키(Cookie)는 [[웹 브라우저]]와 [[웹 서버]] 간의 상태 정보를 저장하고 주고받는 데 사용되는 작은 [[Computer/데이터(Data)]] 조각입니다. 쿠키는 [[클라이언트]] 측에서 관리되며, 웹 서버에서 발급되고 사용자의 [[웹 브라우저]]에 저장됩니다. 이후 해당 웹 사이트를 방문할 때마다 브라우저는 저장된 쿠키를 서버로 다시 전송하여 상태 정보를 유지하거나 개인화된 서비스를 제공하는 데 사용됩니다.

쿠키는 다음과 같은 주요 특징을 갖고 있습니다:

1. **상태 유지(State Management)**: 쿠키는 웹 서버와 클라이언트 간의 상태 정보를 유지하는 데 사용됩니다. 예를 들어, 로그인 정보, 세션 ID, 사용자 환경 설정, 장바구니 내용 등과 같은 정보를 저장하고 유지할 수 있습니다.

2. **도메인 및 경로 제한**: 쿠키는 특정 도메인과 경로에 대해 설정될 수 있으며, 이를 통해 특정 웹 사이트 또는 서브디렉터리에서만 사용될 수 있도록 제한할 수 있습니다.

3. **만료 날짜 및 시간**: 쿠키에는 만료 날짜 및 시간을 설정할 수 있으며, 만료 날짜가 지나면 브라우저는 해당 쿠키를 삭제합니다. 이를 통해 일시적인 [[세션]] 쿠키와 장기적인 지속 쿠키를 구분할 수 있습니다.

4. **보안 및 안전성**: 쿠키는 클라이언트 측에 저장되므로 기본적으로 보안 상태 정보를 저장하기에 적합하지 않습니다. 하지만 쿠키에는 옵션으로 "HttpOnly"와 "Secure" 속성을 추가하여 보안을 강화할 수 있습니다. "HttpOnly" 쿠키는 [[JavaScript]]로 접근할 수 없으며 "Secure" 쿠키는 암호화된 [[HTTPS(하이퍼텍스트 전송 프로토콜 보안, Hypertext Transfer Protocol Secure)]] 연결을 통해서만 전송됩니다.

5. **크기 제한**: 쿠키는 클라이언트 측에서 저장되므로 브라우저마다 저장 가능한 쿠키의 최대 크기가 있습니다.

6. **여러 도메인 간 공유 제한**: 쿠키는 보안상의 이유로 여러 도메인 간에 공유할 수 있는 제약이 있으며, 일반적으로 동일한 도메인 내에서만 공유됩니다.

쿠키는 주로 사용자 인증, 세션 관리, 사용자 추적, 장바구니 저장, 개인화된 경험 제공 등 다양한 웹 애플리케이션에서 활용됩니다. 웹 브라우징 세션 동안 정보를 유지하고 공유하기 위한 간단하고 유용한 수단으로 널리 사용됩니다.