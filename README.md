# devlog_blog_project
블로그 개발 프로젝트

## 12월 20일
+ 블로그 메인페이지 html로 레이아웃 설계
    + 상단 header
    + 사이드 카테고리
    + 메인영역
    + footer 

## 12월 21일
+ 블로그 대분류카테고리 상세페이지 html로 레이아웃 설계
    + 상단 header
    + 사이드 카테고리
    + 대분류 카테고리에 속한 소분류 카테고리를 보여주는 메인영역
    + footer
+ 개선해야 하는 사항
    + 각 페이지별로 중복되는 영역을 효율적으로 처리할 수 있는 방법에 대한 고민 필요


## 12월 22일
+ 블로그 소분류 카테고리 상세페이지 html로 레이아웃 설계
  + 상단 header
  + 사이드 카테고리
  + 상세 게시글 영역
  + footer
+ 개션히야 하는 사항
  + css 레이아웃을 사용하여 영역을 분리하는 방법에 대한 고민 필요

  ## 12월 23일
  + 블로그 게시글 작성 페이지 html 과 css로 레이아웃 설계
   + 상단 header
   + 카테고리 선택하는 부분
   + 글 작성하는 부분
   + 글 저장 버튼
  + 잘된 부분
    + div 태그를 display: inline-block을 사용하여 큰 영역을 먼저 잡고 속 내부를 채웠다
    + 카테고리별 게시글 상세페이지
      + 이미지가 inlne-block 속성이고 이미지 밑에 텍스트를 오게 하고싶은 경우
        + 텍스트를 p태그를 사용하였다 
        + 왜냐하면 p태그는 block 태그 이기 떄문이다
  + 개선해야 하는 사항
    + div 태그를 display: inline-block을 사용하지 않고 수평정렬하는 방식에 대한 고민 푤요

 ## 12월 24일
 + 블로그 로그인 , 회원가입 화면 html 과 css로 레이아웃 설계
 + 상단 header
  + 블로그 로고
  + 버튼들

+ 잘된 부분
  + float를 사용하여 div 레이아웃을 나누고 작업한 부분
    + 전에는 div 정렬하는 것에 어려움이 있었는데 float을 쓰니 정렬이 편해졌다
  + block 특성을 갖는 button태그를 div 안에서 가운데 정렬
    + margin: auto; 속성값을 통해 가운데 정렬

+ 개선해야 하는 사항
  + float을 clear:both 한 이후에 div 에 margin-top이 안먹는 이유
    + display: inline-block 한후 margin-top 속성 값을 줌

  + div 안에서 내부 div를 가로 세러 가운데 정렬하는 방법
    + margin: auto; 
      + 좌 , 우를 기준으로 가운데 정렬

  + div 내부에서 input 태그를 가운데 정렬하는 방법

  + div 내부에서 button 가운데 정렬하는 방법
    + position: relative;
    + top , left 속성을 사용하여 가운데를 맞춰줬다
    + 부모요소의 크기를 기준으로 top , left 방향으로 이동하겠다
    + 참고 - https://velog.io/@younoah/css-centering

  + div 내부에서 block 태그 위 , 아래 가운데 정렬
    + verticle-align: middle; -> 세로 가운데 정렬
    + text-align: center; -> 가로 가운데 정렬
    + 참고 - 참고 - https://moonhouse.co.kr/html/400278
