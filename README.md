# kakao-clone

kakao desktop app clone

HTML

<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- 
        head 태그는 유저에게 보이지 않는다. 
        웹사이트에 관한 필요한 정보를 제공할 뿐이다.
    -->

    <meta charset="UTF-8" />
    <meta name="author" content="Nomad Coders" />
    <meta name="description" content="Welcome to my Kakao Clone" />

    <!--
        meta란 엑스트라, 추가 정보와 같은 뜻.
        content는 웹사이트 검색시 제목 아래에 있는 설명같은 내용이 표시된다.
    -->
    <title>This is my title</title>

  </head>

  <body>
    <section>
      <header id="headerNumberOne" class="defaultHeader">
        <!--
              id는 여권번호처럼 고유하며 class는 국적처럼 여러개 존재할 수 있다.
              즉 id는 태그당 하나의 id만 가질수 있고 class는 여러개 가질 수 있다.
          -->
        <h1>Title of a section</h1>
      </header>
    </section>

    <div>
      <header id="differentHeader" class="defaultHeader">
        Title of the unkown container
      </header>
    </div>

  </body>
</html>

<!--
    semantic Tag - 의미가 있는 태그  ex) h1 ~ h6, header, article, section 등등...

    non-semantic Tag - 아무 의미가 없는 태그  ex) div, span 등등... 박스나 컨테이너 같은 의미로 쓴다.
-->

CSS
/\*
css는 크게 두가지 파트로 나누어져 있다.

    1. selector 파트
    2. property 파트
     - 무조건 소문자

    h1{     -> h1이 selector이다.
        property-name: value;   -> selector 안의 값들이 property이다.
        property-name: value;
        property-name: value;
    }

    id 경우 #id{}
    class 경우 .class{}

\*/

// HTML <---> CSS 연결 방법

<head> 태그 안에 
<link href="styles.css" rel="stylesheet"> 이렇 폼으로 넣어주면 됨.
</head>

// display

- Inline -> 서로 옆으로 붙은 형태, but weith, height 가 없다.
- Block -> 박스들이 밑에 붙는것
- Inline Block -> 박스들이 옆에 붙는것!
- flex -> 부모 박스에만 적용한다. 창이 줄어들어도 그창에 마춰 조절된다. 위의 옵션들로 처리시 자동으로 조절되지 않고 아래로 이동한다. 부모에 flex를 선언하면 아래 자식들이 움직인다.

// Position

- static -> 보이는 시점 이외에 전체화면에 표시. 디폴트 값.
- fixed -> 보이는 시점의 화면에서 위치 고정
- absolute -> absolute로 설정되면 해당 element와 관계있는(relative-부모박스) element를 살펴보고 이에 상응하는 포지션이 결정됨. 없으면 body에 마춰 포지션을 잡는다.
- relative -> 부모박스를 지정해준다. absolute 포지션을 상대적으로이용하려면 부모 element에 꼭 relative를 붙여준다.

justify-content

- 수평관련 정렬

align-item

- 수직관련 정렬

flex-direction

- 출력 방향

// pseudo-selector
가상 셀렉터 만드는법

<=== 1 ===>

<style>
input[type="password"]{
  background-color : blue;
}
</style>

<input type="password">

<=== 2 ===>
.box:last-child{
background-color: pink
}

클래스인 box선언후 가상 셀렉터 last-child이용해 적용
last-child은 모든박수중 마지막 박스를 가리킴.
반대로 처음은 first-child 이다.
child(n) 배열처럼 선택 가능함.

위같이 input의 type password를 스타일 지정해 사용하면 옵션처럼 파랑색컬러가 입혀진다.
html 태그, id, class 없이 스타일을 입힐 수 있다.

// css - states

- active, focus, visited, hover 등등이 있다.
- .box:hover{} (클래스,id 이후 : <- 해주면 states에 접근할수 있다.)
  ex)
- hover - 마우스를 오버 할때 이밴트
- active - 클릭할때 이벤트
- focus - 선택 되었을때 이벤트

<style>
    .box{
      background-color:red;
      font-size: 40px;
    }

.box:hover{
background-color:pink;
}
</style>

<span class="box">lalalalala</span>

// Transitions (트랜지션)

ex)

<style>
      .box {
        background-color: green;
        transition: all 1s ease-in-out; <- 트랜지션 사용법
      }
      .box:active {
        background-color: blue;
      }
</style>

// transformations (트렌스포메이션)

- html문서의 element들을 변경, 모습이 변하는 효과.
- transfrom 내용 관련 링크
  https://developer.mozilla.org/en-US/docs/Web/CSS/transform
- transfrom 과 transition을 같이 적용하면 재미있는 효과를 줄수 있다.

.box {
transform: rotate(20deg);
}

// Animations

- 키프레임 선언 후 애니메이션 이름 작성.
- 스테이지 별로 0-50-100 또는 from - to
- 원하는 효과 transform, transition 을 적용 한다.
- animation 프로퍼티로 효과 적용.

<style>
      .box {
        width: 500px;
        height: 500px;
        background: red;

        animation: 1.5s scaleAndRotateSquare infinite ease-in-out;
      }

      @keyframes scaleAndRotateSquare {
        from {
          transform:none;
        }
        to {
          transform: rotate(1turn) scale(.5, .5);
        }
      }
</style>
