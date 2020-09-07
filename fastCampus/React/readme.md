React 입문
=================

1 소개
------------------
1. 모든 내용은 패스트캠퍼스(이하 패캠)강의 기준으로 작성한다
2. 현재 강의의 내용은 <https://react.vlpt.us/> 참조 가능
3. 함수형 컴포넌트를 기준으로 작성한다.
4. 정리 환경을 위하여 <https://codesandbox.io/s/blazing-firefly-pe0th?file=/src/App.js> 참조 가능 

2 React란? (작업환경 구성)
---------------------------
1. javascript를 사용한 DOM변형 
  * DOM을 관리하기가 어려워지고 이벤트가 많아짐 
  * 각 DOM에 속성에 소속된 이벤트가 꼬이기 시작...
  * 유지보수가 어려워짐 

2. React
  * Virtual DOM을 사용하여 성능을 지키면서 사용 
  * 기존에는 어떻게 업데이트 할지가 아닌 어떻게 보여줄지에 집중!!
  * UI는 컴포넌트 기반으로 선언(UI 조각)

3. 작업환경
  * Node.js (자바스크립트 런타임) 
  * yarn (자바스크립트 패키지 매니징) -> npm보다 빠름
  * VS Code 
  * 혹은 codesandbox를 이용


3 first React Component
---------------------------
1. Hello.js(컴포넌트)
```javascript
import React from 'react';

function Hello() {
  return <div>안녕하세요</div>
}

export default Hello;
```

2. App.js(실행파일)
```javascript
import React from "react";
import Hello from './Hello.js';

function App() {
  return (
    <div>
      <Hello /> {/* 컴포넌트 */}
    </div>
  );
}

export default App;
```