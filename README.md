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

HTML <---> CSS 연결 방법

<head> 태그 안에 
<link href="styles.css" rel="stylesheet"> 이렇 폼으로 넣어주면 됨.
</head>

display

- Inline -> 서로 옆으로 붙은 형태, but weith, height 가 없다.
- Block -> 박스들이 밑에 붙는것
- Inline Block -> 박스들이 옆에 붙는것!
