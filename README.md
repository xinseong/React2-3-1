React2-3-1 

## 201930341윤민성   
<br>

## Next.js
   
- react를 위해 만든 오픈소스  
- 자바스크립트 웹 프레임워크
- 리엑트에 없는 다양한 기능을 제공

### 특징

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


### Next.js가 제공하는 새로운 기능

>코드 분할(SpLitting): 페이지를 로딩 할 때 번들을 여러 조각으로 나누어 필요한 부분만 전송하는 방식

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
### CSR을 사용할 때의 주요 이점 
* 전체 자바스크립트 번들을 다운로드한다는 것은 렌더링할 모든페이지가 이미 브라우저에 다운로드 되어 있다는 뜻
* 다른 페이지로 이동해도 서버에 요청할 필요없이. 바로 페이지를 이동할 수 있습니다.
* 페이지를 바꾸기 위해 새로 고칠 필요가 없습니다.

### 쉬운 페이지 전환
* 클라이언트에서 내비게이션은 브라우저 화면을 새로 고칠 필요 없이 다른 페이지로 이동을 가능 
* 페이지 간 전환에 멋진 효과를 넣을 수도 있습니다. 애니메이션을 방해할 요소가 없기 때문입니다. 




# 동작 컴포넌트 로딩
* 앞서 React.useEffect 혹을 사용하여 브라우저에서 코드를 실행하는 경우에만 컴포넌트를 렌더링 한다.
* dynamic 함수로도 똑갈이 동작하게 할 수 있다.

# 라우팅 시스템
* eact의 React Router, Reach Router 등은 클라이언트 라우팅만 구현할 수 있습니다.
* Next는 파일시스템 기반 페이지와 라우팅을 합니다.

## 동적 라우팅

* /pages/posts/[slug].js 파일을 생성하고 다음과 같이 useRouter를 사용하면 파라메터를 사용할 수 있다.
* ��대괄호는 반드시 사용해야 하고, slug는 pid, category 등 원하는 것을 넣으면 된다.

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


### layout 속성값

* fixed -> 이미지 크기 유지
* Responsive -> 이미지를 최적화해서 제공
* Intrinsic -> fixed와 responsive를 절반씩 수용합니다. 크기가 작은 화면에서는 이미지 크기를 조절하고, 이미지보다 큰 화면에서는 이미지 크기를 조절하지 않습니다.
* fill -> 부모 요소의 가로와 세로 크기에 따라 이미지를 늘림 fill을 사용할 경우 width와 height 사용 불가.

#### 메타데이터

* 페이스북의 오픈 그래프처럼 공유 자료를 카드 형태로 보내려면 몇가지 메타 데이티를 추가해야 합니다.
* Next.js 에서는 내장 Head 컴포넌트를 제공하여 이런 메타 데이터를 쉽게 다를 수 있습니다.

### app.js 와 _document.js 페이지 커스터마이징

```
import * ../styles/globals.css
    
    function MyApp(( Component pageProps )) {
      return <Component {…pageProps} />;
    }

  export default MyApp;
```
* 이 MyApp 컴포넌트와 그 속성인 pageProps를 반환합니다.
* 이에 앞서 제작한 Navbar 컴포넌트를 추가 하면 더 이상 index, about,contact 페이지에 Navbar 컴포넌트를 추가하지 않아도 된다.

