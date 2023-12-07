### 1. crossorigin

    <script
    src="https://unpkg.com/react@18/umd/react.development.js" crossorigin> </script>

> crossOrigin 속성은 element가 CORS 요청을 처리하는 방식을 명시하여 element가 fetch한 데이터를 CROS 가능하게 해준다

### 2. CROS (교차 출처 리소스 공유)

> 추가 HTTP 헤더를 사용하여, 한 출처에서 실행 중인 웹 에플리케이션이 다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여하도록 브라우저에서 알려주는 체제임

### 3. [JSX](https://ko.legacy.reactjs.org/docs/introducing-jsx.html)

> JavaScript를 확장한 문법. 생긴 게 HTML 이랑 비슷해서 JSX로 React 요소를 만드는 게 편리함

babel로 jsx 코드를 브라우저가 이해할 수 있는 형태로 바꿔줌

### 4. useState()
배열의 첫번째 값은 초기값, 두번째 요소는 그 값을 바꾸는 함수임 <br>
함수를 사용해서 어플리케이션의 데이터를 바꿀 때 컴포넌트는 새로운 값을 가지고 리렌더링을 함

    let counter=0;
    function  countUp(){
        counter+=1
    }

    =>
    const [counter, setCounter] = React.useState(0);

현재 state를 바탕으로 다음 state를 계산할 때 이런 식으로 함수 전달해야 함

    const onClick = () => {
        setCounter((current) => current + 1); 
      };