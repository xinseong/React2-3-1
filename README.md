React2-3-1 

## 201930341윤민성   
<br>

## Next.js
   
- react를 위해 만든 오픈소스  
- 자바스크립트 웹 프레임워크
- 리엑트에 없는 다양한 기능을 제공

## 특징

- 서버 사이트 렌더링(SSR)
- 정적 사이트 생성(SSG)
- 증분 정적 재생성(ISR)
   
> SSG는 미리 만들어 놓은 페이지를 서비스 하기 때문에 속도가 빠름
하지만 한번 생성하면 수정이 불가능하다.

> 이러한 단점을 보완하고자 IRS가 나옴
이미 생성된 페이지를 일정 시간이 지난 후에 다시 생성(최신 데이터로 업데이트)

## Next.js란?
 
 Angular, React, Vue 와 같은프레임워크가 등장하면서 웹 개발 분야는 급속도로 변하기 시작.

- 리액트는 페이스북(메타)의 조던 발케가 만들어, 2013년 오픈소스를 발표합니다.

- 리엑트는 클라이언트 사이에서만 작동한다는 문제점이 있습니다.

- 이 문제를 해결하기 위해 서버에서 미리 렌더링해 두는 방법을 연구하기 시작합니다.

- 이러한 연구의 결과로 나온 것이 Next.js입니다.

- 이로써 리액트가 제공하지 않는 여러가지 기능을 제공하게 됩니다.


## Next.js가 제공하는 새로운 기능


*   서버 사이트 렌더링
*   파일 기반 라우팅
* 경로 기반 프리페칭

>(Prefetching) : 사용자가 다음에 이동할 수 있는 페이지를 미리 가져오는 기술.

*   정적 사이트 생성
*   증분 정적 콘텐츠 생성
*   타입스크립트에 대한 기본 지원
*   자동 폴리필 (Polyf111) 적용: 이전 브라우저에서 최신 기능을 제공하는 데 필요한 코드를 제공.
*   이미지 최적화 : Next/image 컴포넌트로 제공하는 이미지의 최적화 기술
*   웹 애플리케이션의 국제화 지원: 다국어 지원
*   성능 분석

## 리엑트에서 Next.js로

*   Next js의 기본 철학은 React와 거의 같습니다.

* “Convention over configuration”은 개발자가 해야 할 결정의 수를 줄여주면서도 유연성은 잃지 않도록 하는 소프트웨어 설계 패러다임입니다.

*   예를 들면 설정 파일을 만들지 않고도 어떤 페이지에 서버 사이드 렌더링을 적용하 고, 어떤 페이지에 정적 페이지 생성을 적용할지 지정할 수 있습니다.

*   Next.js는 fetch, window, document와 같은 웹 브라우저에서 제공하는 전역 객 체나 canvas 같은 HTWL요소에는 접근 할 수가 없습니다.

*   전역 객체나 HTML요소를 반드시 사용해야 하는 컴포넌트를 다루는 방법을 별도로 제 공합니다. 

*   반면 fs, child_proces와 같이 Node• js에서만 사용할 수 있는 라이브러리나 API 를 사용하려는 경우,각 요청 별 데이터를 클라이언트로 보내기 전에 서버 사이드 코드를 실행하거나 페이지 생성 시점에 해당코드를 처리하는 방식을 지원합니다.
    + 어떤 방식으로 지원하는지는 각 페이지가 어떤 렌더링 방식을 사용하는가에 따라 결정됩니다.

*   클라이언트 사이드 앱, 프로그레시브 웹 앱, 오프라인 웹앱 도 쉽게 만들 수 있습니다.

*   많은 내장 컴포넌트와 최적화 기능을 사용할 수 있다는 장점도 있습니다.

* Progressive Web Apps(PWA)은 웹 앱과 네이티브 앱의 장점을 모두 제공합니다.

## 프로젝트 생성 방법
*  create-next-app을 이용하여 프로젝트를 생성해 봅니다.
<pre>
<code>
npx create-next-app 앱이름
</code>
</pre>

*  프로젝트가 생성되면 프로젝트 디렉토리로 이동하여 다음 명령을 실행합니다. 

<pre>
<code>
npm run dev
</code>
</pre>


* React처럼 바로 실행되지 안기때문에 http://localhost3000 으로 접속하여 확인. (Ctrl + 클릭하면 실행.)

* 만일 개발환경에 yarn 패키지가 설치되어 있다면 Next.js는 yam을 사용하여 프로젝트를 초기화 합니다.

* (yarn이 설치되어 있을 때 ) npm을 기본으로 사용하고 싶다면 


<pre><code>
npx create-next-app 앱이름 - use-npm
</code></pre>

## 프로젝트의 기본 구조

* Nextjs는 네비게이션을 구현할 때 react-router와 같은 라이브러리를 사용하지 않고, pagel 디렉토리를 사용합니다.

* pages/ 디렉토리 안의 모든 js파일은 public 페이지가 됩니다.

*  pages/ 의 indexjs파일을 복사해서, aboutjs로 이름을 바꾸면,http://localhost5000/about 으로 접속할 수 있습니다.
  
* public/ 디렉토리에는 웹 사이트의 모든 퍼블릭 페이지와 정적 콘텐츠가 있습
  - 이미지, 컴파일된 cSs, 컴파일된. is, 폰트 등.

* styles/ 디렉토리에는 앱에서 사용하는 스타일시트 넣습니다.
  - 하지만 이 디렉토리가 필수는 아님

*  용도가 정해져 있는 디렉토리는 pages/ 와 public/ 뿐입니다.

*  나머지 디렉토리는 필요에 따라서 다른 목적으로 사용하거나 삭제해도 됩니다.
  - 프로젝트 root에 필요한 디렉토리를 새로 생성해서 사용가능

  ## 타입스크립트 지원

* Nextjs는 타입스크립트로 작성되었기 때문에 고품질의 type definition을 지원합니다.

* 기본 언어를 타입스크립트로 지정하려면 root에 tscontig.json이라는 설정파일 생성하면 됩니다.

* 그런 다음 npm run dev 명령을 실행하면 다은과 같은 메시지를 확인할 수 있습니다.
  - 패키지를 설치하고 나면 비어 있던 tsconfig.json 파일의 내용이 자동으로 채워집니다.

```
npm i -g create-react-app

npx create-next-app test1
```
SWC 사용   
```
npx create-next-app @latest test1  
```

만일 기본 웹팩 설정을 바꾸고 싶다면 webpack이라는 키에 해로운 속성값을 지정합니다.

```
module. exports = {
webpack: (config, options) =› {
config.module.rules.push({
test: /\.js/, 
use: [
options.defaultLoaders.babel,
//이 부분의 내용은 예시이기 때문에
//실제로 사용하면 애플리케이션이 작동하지 않습니다.
{loader: "ay-custon-loader*, //사용할 로더 지정
options: loaderOptions,// 로더의 옵션 지정},
],
});
return config;
},
}
```
*   이 페이지는 div 요소 안에 문자열인 표시합니다.
*   외부 AP를 호출 하지 않으며 항상 같은 문자열만 표시됩니다.

* 다음 코드는 페이지를 요청할 때마다사용자 환영 문구를 표시합니다.
* 특정 사용자 정보를 가져온 다음클라이언트에 전달해서 사용할 수 있도록 하고 있습니다.
* 이 경우 미리 예약된 getServerSide Props() 함수를 사용합니다.

```
import React from 'react';

export async function getServerSideProps() {
  const userRequest = await fetch("https://example.com/api/user");
  const userData = await userRequest.json();

  return {
    props: {
      user: userData,
    },
  };
}

function IndexPage(props) {
  return <div>Welcome, {props.user.name}!</div>;
}

export default IndexPage;

```

* getServersideProps라는 비동기 함수를 export합니다.
* getServerSideProps 함수는 props라는 속성값을 갖는 객체를 반환합니다.props는 컴포넌트로 전달되어 서버와 클라이언트 모두가 props에 접근할 수 있게 됩니다.
* IndexPage 함수를 수정해서 props를 인자로 받습니다.

### 컴포넌트 생성
```
import React from 'react';

function MyComponent(props) {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
}

export default MyComponent;
```

### 컴포넌트 사용
```
import React from 'react';
import MyComponent from './MyComponent'; // 컴포넌트 파일의 경로에 맞게 수정

function App() {
  return (
    <div>
      <MyComponent title="제목" description="이것은 설명입니다." />
    </div>
  );
}

export default App;
```
## 이미지 넣기
```
import Image from "next/image";

export default function ImagePage(){
  return (
    <>
      <div style={{
        width: 500,
        height: 200,
        position: 'relative'
      }}>
        
       <Image 
        src='https://cdn.pixabay.com/photo/2023/09/06/12/21/waves-8236919_1280.jpg' 
        layout="fill" 
        objectFit="cover" 
        alt="test image"      
      />
      </div>
    </>
  )
}

```
## CSR을 사용할 때의 주요 이점 
* 전체 자바스크립트 번들을 다운로드한다는 것은 렌더링할 모든페이지가 이미 브라우저에 다운로드 되어 있다는 뜻
* 다른 페이지로 이동해도 서버에 요청할 필요없이. 바로 페이지를 이동할 수 있습니다.
* 페이지를 바꾸기 위해 새로 고칠 필요가 없습니다.

## 쉬운 페이지 전환
* 클라이언트에서 내비게이션은 브라우저 화면을 새로 고칠 필요 없이 다른 페이지로 이동을 가능 
* 페이지 간 전환에 멋진 효과를 넣을 수도 있습니다. 애니메이션을 방해할 요소가 없기 때문입니다. 




## 동작 컴포넌트 로딩
* 앞서 React.useEffect 혹을 사용하여 브라우저에서 코드를 실행하는 경우에만 컴포넌트를 렌더링 한다.
* dynamic 함수로도 똑갈이 동작하게 할 수 있다.

## 라우팅 시스템
* eact의 React Router, Reach Router 등은 클라이언트 라우팅만 구현할 수 있습니다.
* Next는 파일시스템 기반 페이지와 라우팅을 합니다.

## 동적 라우팅

* /pages/posts/[slug].js 파일을 생성하고 다음과 같이 useRouter를 사용하면 파라메터를 사용할 수 있다.
* 대괄호는 반드시 사용해야 하고, slug는 pid, category 등 원하는 것을 넣으면 된다.

```
import { useRouter } from 'next/router'

const Post = () => {
  const router = useRouter
  //{"pid": "foo"}, {"pid": "bar"}
  const { pid }= router.query
  return <p> Post: {pid} </p>

}
export default Post
```
## 페이지에서 경로 매개변수 

* 내장 getServerSideProps 함수를 통해 URL에서 동적으로 [name] 변수 값을 가져온다.

```
export async function getServerSideProps (( params )){

  const { name } = params;
  return {
    props: ( name,
    );
  }
  function Greet (props) {
  return {
    <h1> Hello, (props.name)! </h1>
    };
  }
}
export default Greet;
```
## 네비게이션
* Link 컴포넌트를 사용하여 서로 다른 페이지 간의 이동을 최적화 할 수 있다.
* 다른 페이지 또는 웹 사이트의 일부를 연결할 때 Link컴포넌트 사용
* 화면 전환 속도가 빠른 이유

```
import Link from 'next/link';

function Navbar() { 
  return (
  <div>
    <Lick href-'/about'>Home</Link>
    <Link hrefs' /about '>About </Link>
    <Link href-'/about"›Contact</Link> 
  <dlv>
  );
}
```

#### router.push 메서드

* Link 컴포넌트 대신 useRouter Hook을 사용해서 다른 페이지로 이동 가능
* 클라이언트에서의 네비게이션 구현에 router.push를 사용하는 것은 비추천

#### 자동 이미지 최적화
* 이 기능을 사용하면 이미지를 최신 이미지 포맷으로 제공할 수 있습니다.
* 최신 포맷을 지원하지 않는 브라우저의 경우에는 png나 jpeg와 같은 예전 이미지 포맷도 제공.


#### layout 속성값

* fixed -> 이미지 크기 유지
* Responsive -> 이미지를 최적화해서 제공
* Intrinsic -> fixed와 responsive를 절반씩 수용합니다. 크기가 작은 화면에서는 이미지 크기를 조절하고, 이미지보다 큰 화면에서는 이미지 크기를 조절하지 않습니다.
* fill -> 부모 요소의 가로와 세로 크기에 따라 이미지를 늘림 fill을 사용할 경우 width와 height 사용 불가.

7주차
#### 메타데이터

* 페이스북의 오픈 그래프처럼 공유 자료를 카드 형태로 보내려면 몇가지 메타 데이티를 추가해야 합니다.
* Next.js 에서는 내장 Head 컴포넌트를 제공하여 이런 메타 데이터를 쉽게 다를 수 있습니다.

## app.js 와 _document.js 페이지 커스터마이징

```
import * ../styles/globals.css
    
    function MyApp(( Component pageProps )) {
      return <Component {…pageProps} />;
    }

  export default MyApp;
```
* 이 MyApp 컴포넌트와 그 속성인 pageProps를 반환합니다.
* 이에 앞서 제작한 Navbar 컴포넌트를 추가 하면 더 이상 index, about,contact 페이지에 Navbar 컴포넌트를 추가하지 않아도 된다.

## 다크모드

```
다크모드 설정
const { createContext } = require("react");

const ThemeContext = createContext({
	theme: 'light'
	toggleTheme: () => null
})

export default ThemeContext

_app.js
const themes = {
	dark: {
		background:’black’,
		color:’white’
	},
light: {
	background:’black’,
	color:’white’
}
}
```
### document.js 페이지

* Next페이지에서는 <html>,<head>,<body>와 같은 기본적인 HTML 태그를 정의할 필요가 없습니다.
*   Head 컴포넌트에서 이 태그를 제공하고 있습니다.
*   puges/_documentjs 파일로 기능을 확장할 수 있습니다.

8주차
### Rest API 호출

```
export async function (getServerSideProps) {

//여기에 REST API를 호출합니다.
const userReg = await axios.get('hetps: //dummy. restapiexample. com/api/vi/employees’);

	return {
		props: {
			users: userReq.employee_name,
		},
	}
}
```
9주차

## 디렉토리 구조 구성

* Node modiles/ : Nextjs 프젝트의 의존성 패키지를 설치하는 디렉토리
* pages/ : 애플리케이션의 페이지 파일을 저장하고 라우팅 시스템 관리
* public/ : 컴파일된 CSS 및 자바스크립트 파열, 이미지, 아이콘 등의 정적 자원 관리
* styles/ : 스타일링 포맷(CSS, SASS, LESS 등)과 관계없이 스타일링 모듈 관리
* pages/ 디렉토리를 ac/ 디렉토리 안으로 옮길 수 있습니다.
* public/과 node modules/ 를 제외한 다른 디렉토리는 모두 C/ 로 옮길 수 있습니다.


## 컴포넌트 구성
* 컴포넌트는 세 가지로 분류하고 각 경포넌트와 관련된 스타일 및 테스트 파일을 같은 곳에 두어야 합니다.
* 코드를 더 효율적으로 구성하기 위해 아토믹 디자인 원칙에 따라 디렉토리를 구성합니다.
* atoms : 가장 기본적인 컴포넌트 관리. button, input, p와 같은 표준 HTML요소를 감싸 는 용도로 사용되는 컴포넌트
* molecules : atom에 속한 컴포넌트 여러 개를 조합하여 복잡한 구조로 만든 컴포넌트 관리.input과 label을 합쳐서 만든 새로운 컴포넌트
* organisms : molecules와 atoms를 섞어서 더 복잡하게 만든 컴포넌트 관리.footer나carousel 컴포넌트
* templates : 위의 모든 컴포넌트를 어떻게 배치할지 결정해서 사용자가 접근할 수 있는 페이지


## 정적 자원의 구성
* 정적 자원은 public/ 디렉토리에서 관리합니다.
* 일반적인 웹 애플리케이션에서는 다음과 같은 정적 자원을 사용합니다.
    - 이미지
    - 컴파일한 자바스크립트 파일 컴파일한 CSS 파일
    - 아이콘
    - 정적 파일
* 먼저 public/assets/ 디렉토리를 만들고 파일 유형별로 다시 디렉토리를 추가 합니다.
* 그리고 이곳에 저장된 파일에 접근하고자 하면 예와 같이 public을 제외한 주소를 써주면 됩니다.


## lib 파일 수성
* lib 파일은 서드파티 라이브러리를 감싸는 스크립트를 말합니다.
* lib 파일은 특정 라이브러리에 특화된 것입니다.GraphQL 만일 GraphQL을 사용한다면, 클라이언트를 초기화 하고, 질의문과 뮤테이션을 저장하는 등의 작업이 필요합니다.
* 먼저 이런 스크립트를 좀 더 모듈화하기 위해 프로젝트 root에 lib/graphql/ 디렉토리를 듭니다.


## ssr-rest-api

* 먼저 새로운 Next 프로젝트를 생성합니다.
    - прх create-next-app ssr-rest-api
* Axios 패키지를 추가합니다. S npm install axios 
* 이번 프로젝트는 public API를 호출하여 몇몇 상용자의 등과 1D를 표시해 봅니다.
* 사용자 이름을 클릭하면 세부 페이지로 이동해서 사용자 정보를 자세히 볼 수 있도록 만듭니다.


## 클라이언트가 데이터 불러오기

* 동적 웹앱에서는 클라이언트가 데이터를 불러오는 경우가 많습니다.
* 그러나 서버가 데이터를 불러오는 것이 좀 더 안전합니다.
* API 엔드포인트 주소, 매개변수 값, HTTP 헤더, 인증 토큰 값 등 중요한 정보가 외부에 노 출되지 않기 때문입니다.
* 브라우저에서 HTTP요청을 보낼 때는 반드시 다음 사항을 지켜야 합니다.
    - 믿을 수 있는 곳에만 HTTP요정을 보내야 합니다.
    - SSL 인증서를 통해 안전하게 접근할 수 있는 곳의 HTTP API만 사용해야 합니다.
    - 브라우저에서 원격 데이터베이스에 직접 연결해서는 안 됩니다.


## csr-rest-api


* 첫 번째: return 안을 보면, "Loading users.. 문자열 가지고 있습니다. HomePage컴포넌트의 초기 강태입니다.
* 두 번째: 리엑트 하이드레이션이 일어난 후에야 사용자 목록을 볼 수 있습니다.
* 클라이언트는 컴포넌트가 마운트된 후에 브라우저의 fetch API를 사용해서 HTTP 요청을
* 보냅니다.
* 사용자 상세 페이지를 다음 순서대로 만들어 봅니다.
* pages/users/lusernamelJs 파일생성 》 getServersideProps함수 만들기 》 경로 매개변 수 [username]과 .env의 인증 토큰 값 가져오기.


* 원격 서버에서 데이터를 가져오는 경우 CORS 문제가 쉽게 발생합니다.
* 클라이언트에 인증 토큰을 노출한다는 점입니다.
* Network 탭을 보면 특정 엔드포인트로 보낸 HTTP 요정을 볼 수 있습니다.
* 이 요청의 헤더를 보면 평문으로 된 인증 토큰값을 확인할 수 있습니다.

* pages/api/singleUserjs 파일을 만들고 다음과 같이 코딩합니다.

```
import axios from 'axios’;

export default async function handler(red,rest){
	const username =  reg. query.username;
	const API_ENOPOINT = process. env.API_ENDPOINT; 
	const API_TOKEN = process.env.API_TOKEN;
	
	const userRed Baalt axios.get(
	’S(API, ENDPOINT) /api/04/users/$(username)*,
	{headers: ( authorization: API,TOKEN ) }
);
	res. status (200). json(userReg.data);
}
```
## GraphQL API

* API에서 사용할 수 있는 질의어로 REST SOAP 같은 방식과는 다른 새로운 관점으로 API데이터를 다릅니다.
* 꼭 필요한 데이터만 불러오도록 지정할 수 있습니다.
* 한 번의 요정으로 여러 곳의 데이터를 불러올 수 있습니다.
* 사용할 데이터에 대해 정적이면서도 강력한 타입 시스템을 제공합니다.
* 여기서는 Apollo 클라이언트를 사용합니다.
* Apollo는 많이 사용되는 GraphqL 클라이언트로, react와 next를 기본으로 지원합니다.


## signbook		lib/apollo/index.js

* Apollo 클라이어트를 초기화하기 위한 함수를 추가합니다. 113페이지 하단의 코드.
* 이 함수를 사용하면 페이지마다 새로운 Apollo 클라이언트를 만들지 않아도 됩니다.
* 대신 클라이언트 인스턴스를 apolloClient 변수에 저장하여, 인스턴스를 함수 인자에 초기 상태값으로 전달합니다.
* 해당 함수는 지역 캐시값과 전달받은 초기 상태값을 합쳐서 전체 상태값을 만들어 사용합니다.


## GraphoL 질의문 생성

* 사용할 질의문은 lib/apollo/queries/ 디렉토리 아래 저장해야 합니다.
* 다음 pages/indexjs 파일에서 질의문을 불러와 사용합니다.
```
import {useQuery } from “@apollo/client";import GET_LATEST SIGNS from ‘../lib/apollo/queries/getLatestSigns';

export default function HomePage(){
  const {loading, data } = useQuery(GET_LATEST_SIGNS,fetchPolicy: ('no-cache'));

return <div></div›;
};
```
* useQuery 훅 덕분에 질의 처리와 관련된 다음 세 가지 상태값에 접근할 수 있습니다.

11/23

## 지역 및 전역 상태 관리

* 리액트 앱에서는 상태 관리는 아주 중요한 부분입니다.
* 상태는 동적 정보의 일종입니다.
    - 높은 수준의 상호 작용이 가능한 비 구현하거나,
    - 더 뛰어난 UX 개발 위한 필수 요소입니다.
* 최신 웹앱에서는 비가 상태를 사용하고, 관리하는 경우가 많이 있습니다.
    - 밝은 테마에서 어두운 테마로 변경하거나.
    - 배송 주소를 바꿈으로써 폼의 상태를 변경합니다.
    - 버튼 클릭 만으로 앱의 상태를 변하게 할 수도 있다.
* 상태 관리 때문에 앱에 더 뛰어난 상호 작용 등의 기능을 구현할 수 있지만, 앱의 복잡도는 증가 합니다.
* 지역 상태 관리에 있어서 앱의 상태는 컴포넌트 스코프 상태를 의미합니다.
* Increment버튼을 클릭하면 현재 click하면 Count값에 1을 더하고, Decrement버튼을 클릭하면 현재 값에서 1을 뺍니다.

```
import React, ( useState ) from "react";

export default  function Counter({ initialCount = 0 }){
const [count, setCount] = useState(initialCount);

return (
<div>
	  <b>Count is: (count)</b><br />
	  <button onClick=(() = setCount (count + 1))>
		Increment +
	  </button>
	  <button onClick={() = setCount(count - 1)}>
		Decrement - 
    </button>
	</div›
	);
}

```
### 아톰 컴포넌트 
>비교적 작은 크기로 가장 흔하게 접하는 컴포넌트

### 로딩 상태
* 클라이언트 측에서 외부 데이터를 읽어올 때, 아직 데이터를 다 가져오지 못한 상황입니다.
* 즉, 전송한 HTTP 요청이 아직 끝나지 않은 상태입니다.
* 이런 경우 일반적으로 loading 상태값을 true로 세팅하고, 전송 요청이 끝날 때까지 UI에 스피너 (spinner)아이콘 등을 표시합니다.


## 전역 상태 관리

* 전역 상태는 여러 컴포넌트가 공유하는 상태를 의미합니다.
* 즉, 어떤 컴포넌트라도 접근 및 수정이 가능한 상태인 것입니다.
* Vue.js나 Angular와는 다르게 React는 데이터 흐름이 단방향 입니다.
* 단방향의 데이터 흐름은 
1) 오류 발생 가능성을 줄여 주고, 
2) 디버깅하기 쉬우며 효율적이라는 장점이 있습니다.


## boilerplate

* 선택한 상품을 전역 상태에 저장할 때는 자바스크립트 객체로 저장하는 방법을 사용합니다.
* 각 속성은 상품ID를 의미하며, 이 값은 사용자가 담은 상품의 개수를 나타냅니다.
* data/items.js 파일을 열어보면 여기서 사용할 상품 정보를 확인할 수 있습니다.
* 사용자가 당근 네 개와 양파 두개를 담았을 때의 상태 객체는 다음과 같습니다.



>* 선택한 상품을 전역 상태에 저장할 때는 자바스크립트 객체로 저장하는 방법을 사용합니다.
>* 각 속성은 상품ID를 의미하며, 이 값은 사용자가 담은 상품의 개수를 나타냅니다.
>* data/items.js 파일을 열어보면 여기서 사용할 상품 정보를 확인할 수 있습니다.
>* 사용자가 당근 네 개와 양파 두개를 담았을 때의 상태 객체는 다음과 같습니다.

```
export default function Highlight(props) {
  return(
  <>
    <span>{props. text}</span>
    <style jsx>{' 
      span {
        background: yellow; 
        font-weight: bold;
      }
    '}</style>
  </>
  );
}
```

>* 만일 모든 컴포넌트에 적용할 CSS 규칙을 만들고 싶다면 global 속성을 지정하면 된다.
>* 전역 상태로 사용할 경우 예상하지 못한 결과를 초래할 수 있으니 조심

## CsS-in-JS의 단점

* IDE나 코드 편집기 등 개발 도구에 대한 지원이 부족합니다.
* 문법 하이라이팅, 자동 완성, 린트(int)기능을 제공하지 않습니다.
* 코드 내에서 CSS에 대한 의존성이 점점 커지기 때문에 앱 번들도 커지고 느려 집니다.
* 서버에 미리 CSS를 생성해도 클라이언트에서 리액트 하이드레이션이 끝나면 CSS를 다시 해야 합니다.
* 이 때문에 실행 시점에 부하가 커지며, 웹 앱이 계속 느려지게 됩니다.


## SASS

* Next에서 기본으로 지원하는 전 처리기 입니다.
* 단 패키지 설치가 필요합니다. S npm install sass
* SASS 및 SCSS(Sassy CSS) 문법으로 CSS Module을 만들고 사용할 수 있습니다.
* styles/Home.module.css 파일 이름을 styles/Home.module.scss로 바꿔주면 됩니다.

## Chakra UI

* 오픈소스 컴포넌트 라이브러리로, 모듈화 되어 있고 접근성이 뛰어나며 보기 좋은 비를 만들 수 있습니다.
* 버튼, 모달, 입력 등 다양한 내장 컴포넌트를 제공합니다.
* dark mode 및 light mode를 모두 지원합니다.
* Chakra ul의 useColorMode 흑을 사용해서 현재 사용하는 컬러 모드를 확인할 수 있습니다.

## 테스트란?

> 1. 단위 테스트
코드의 각 함수가 제대로 작동하는지 확인하는 테스트 입니다.
함수에 올바른 입력과 잘못된 입력을 각각 주고 그 결과가 예상과 일치하는지 봅니다.
또한 작동 과정에서 예측하지 못한 오류가 발행하는지도 확인합니다.

>2. 엔드 투 엔드 테스트
앱에 대한 사용자 상호 작용을 흉내내서 특정 작동이 발행했을 때 적절한 응답을 하는지 확인하는 테스트 입니다.
폼 입력이나 css가 적절하가 적용되는지 등을 테스트합니다.

> 3. 통합 테스트
함수나 모듈과 같이 서로 구분되는 영역이 함께 잘 작동하는지 확인하는 테스트 입니다.
서로 연관된 함수와 모듈을 한데 묶어서 주어진 입력에 맞는 적절한 출력을 만들어 내는지 확인합니다.

## Jest를 사용한 단위 테스트와 통합 테스트

1. 자바스크립트 생태계에서 가장 유명한 테스트 러너입니다.
2. 먼저 GitHub 저장소에서 09-testing-nextjs/boilerplate를 클론합니다.
3. 그리고 node모듈을 설치합니다. $ npm !

이제 의존성 패키지를 설치할 차례입니다.

4. 클론한 디렉토리에서 jest를 설치 합니다. S npm i jest --save-dev

페이지 테스트를 만들 때 주의할 점은 다음과 같습니다.
- pages/ 안의 모든 js jsx tS tsx 파일을 앱 페이지로 간주합니다.
- 따라서 소트 파일은 절대 pages/ 안에 작성하면 안됩니다

### iCypress를 사용한 엔드 투 엔드 테스트

* 앱 전체가 잘 동작하는지 확인하는 테스트입니다.
* Cypress는 웹 브라우저에서 돌아가는 모든 것을 테스트할 수 있는 강력한 도구입니다.


1. 관례상 Cypress 엔드 투 엔드 테스트를 위한 디렉토리는 root에 만듭니다. cypress/
2. cypress/integration/api.specjs라는 테스트 파일을 만들고 작성합니다.
3. 작성은 sample 코드를 참고합니다.
4. 코드 작성을 끝내고 명령으로 실행하면 오류가 발생합니다.
> $ npm cypress 
5. Cypress는 실제 서버를 대상으로 테스트를 실행하기 때문에 나는 오류입니다.
6. 이 오류는 다음 패키지 설치로 해결할 수 있습니다.
> $ npm i start-server-and-test—dev
7. 그리고 Cypress 시작 전 서버를 실행할 수 있도록 packages.json의 scripts에 다음을 주가 합니다. 이제 npm e2e를 먼저 실행하고 테스트 하면 됩니다.