# React.js

## React.js란?
리액트(React, React.js 또는 ReactJS)는 자바스크립트 라이브러리의 하나로서 사용자 인터페이스를 만들기 위해 사용된다. 페이스북과 개별 개발자 및 기업들 공동체에 의해 유지보수되며. 리액트는 싱글 페이지(SPA)나 모바일 애플리케이션의 개발시 토대로 사용될 수 있다. 복잡한 리액트 애플리케이션들은 상태 관리, 라우팅, API와의 통신을 위한 추가 라이브러리의 사용이 일반적으로 요구된다.

## 리액트는 어쩌다 만들어졌을까? 
 사용자와의 인터랙션이 별로 없는 웹페이지라면 상관없겠지만, 만약에 인터랙션이 자주 발생하고, 이에 따라 동적으로 UI 를 표현해야된다면, 이러한 규칙이 정말 다양해질것이고, 그러면 관리하기 힘들어짐. 숙련된 JavaScript 개발자라면, 코드를 최대한 깔끔하게 정리하여 쉽게 유지보수를 할 수도 있겠지만, 대부분의 경우 웹 애플리케이션의 규모가 커지면, DOM 을 직접 건드리면서 작업을 하면 코드가 난잡해지기 쉽움.
 그래서, Ember, Backbone, AngularJS 등의 프레임워크가 만들어졌었는데, 이 프레임워크들은 작동방식이 각각 다르지만, 자바스크립트의 특정 값이 바뀌면 특정 DOM의 속성이 바뀌도록 연결을 해주어서, 업데이트 하는 작업을 간소화해주는 방식으로 웹개발의 어려움을 해결.
 리액트의 경우에는 조금 다른 발상으로 리액트는 어떠한 상태가 바뀌었을때, 그 상태에 따라 DOM 을 어떻게 업데이트 할 지 규칙을 정하는 것이 아니라, **아예 다 날려버리고 처음부터 모든걸 새로 만들어서 보여주는 아이디어**에서 개발이 시작
 
## 리액트의 이해
 리액트는 자바스크립트 라이브러리로 사용자 인터페이스를 만드는데 사용함, 구조가 MVC, MVW 등인 프레임워크와 달리. **오직 V(View)만 신경쓰는 라이브러리**
 
### 컴포넌트
  컴포넌트는 재사용이 가능한 API로 수 많은 기능들을 내장하고 있으며, 컴포넌트 하나에서 해당 컴포넌트의 생김새와 작동 방식을 정의

### Virtual DOM

 Virtual DOM을 사용하면 실제 DOM에 접근하여 조작하는 대신, 이를 추상화한 자바스크립트 객체를 구성하여 사용
 - 리액트에서 데이터가 변하여 웹 브라우저에 실제 DOM을 업데이트 할 때 절차
  - 데이터를 업데이트하면 전체 UI를 Virtual DOM에 리렌더링
  - 이전 Virtual DOM에 있던 내용과 현재 내용을 비교
  - 바뀐 부분만 실제 DOM에 적용 // **시간복잡도(N) WOW~!**
  
### SPA
 서버로부터 완전한 새로운 페이지를 불러오지 않고 현재의 페이지를 동적으로 다시 작성함으로써 사용자와 소통하는 웹 애플리케이션이나 웹사이트. 이러한 접근은 연속되는 페이지들 간의 사용자 경험의 간섭을 막아주고 애플리케이션이 더 데스크톱 애플리케이션처럼 동작하도록 만들어줌. SPA에서 HTML, 자바스크립트, CSS 등 필요한 모든 코드는 하나의 페이지로 불러오거나, 적절한 자원들을 동적으로 불러들여서 필요하면 문서에 추가하는데, 보통 사용자의 동작에 응답하게 되는 방식이다. 문서는 프로세스 중 어떠한 지점에서도 다시 불러들이지 않으며 다른 문서로 제어권을 넘기지 않으나, 위치 해시나 HTML5 히스토리 API를 사용하여 애플리케이션 안에서 개개의 논리 문서의 인식 및 탐색을 제공할 수 있다. 싱글 페이지 애플리케이션과의 소통은 뒷편에 있는 웹 서버와의 동적인 통신을 수반하기도 한다.
 
## 환경셋팅
 - Node.js: Webpack 과 Babel 같은 도구들이 자바스크립트 런타임인 Node.js 를 기반으로 만들어져있습니다. 그렇기에 해당 도구들을 사용하기 위해서 Node.js 를 설치합니다.
 - Yarn: Yarn 은 조금 개선된 버전의 npm 이라고 생각면 됨. npm 은 Node.js 를 설치하게 될 때 같이 딸려오는 패키지 매니저 도구. 프로젝트에서 사용되는 라이브러리를 설치하고 해당 라이브러리들의         버전 관리를 하게 될 때 사용. Yarn 을 사용하는 이유는, 더 나은 속도, 더 나은 캐싱 시스템을 사용하기 위함
 ```
 yarn create react-app begin-react
 ```
  ```
 cd begin-react
 ```
  ```
 yarn start
 ```
