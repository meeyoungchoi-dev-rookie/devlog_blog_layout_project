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


  ## 12월 25일
  + 블로그 로그인 회원가입 페이지 레이아웃 수정
    + 잘 한 부분
      + div 내부에서 input 태그를 가운데 정렬하는 방법
        + input 요소의 display 를 inline-block으로 처리
        + margin-left 속성 값을 기존 px 에서 %로 변경
        + input 태그 내의 text를 정렬하기ㅏ 위해 text-align: center 사용

      + float을 clear:both 한 이후에 div 에 margin-top이 안먹는 이유
        + clear: both 처리한 부모 div를 display:inline-block 처리
        + 그후 margin-top 적용

        + 자식 div 가로 세로 가운데 정렬
          + 자식 div의 position을 absolute 처리
          + 부모 div를 position을 relative 처리
          + 부모 div를 기준으로 top , left 속성 값 적용

    + 개선 해야 하는 사항
      + 소분류 카테고리 항목의 글 상세보기 페이지 레이아웃 
        + float , position을 사용하여 레이아웃 수정
    


 ## 12월 26일
   + 블로그 프로젝트 카테고리 소분류 별 글목록 레이아웃 수정
    + float 속성을 사용하여 레이아웃 수정
       * 작업 내용
         + header
         + content
         + footer

      + 잘 된 점
        + float를 사용하여 div 3개를 가로로 정렬 하였다
          + float: left 속성값을 사용하여 div를 왼쪽에 띄운후
          + margin-left 속성으로 여백을 줬다
        + float 처리된 div 밑에 footer div를 만들었다
          + footer div 태그에 float 속성을 제거하기 위해 clear: both를       사용하였다
          + ```
               .content .left_side {
                float: left;
                width: 250px;
                height: 1000px;
                border: 1px solid orange;
                
            }

            .content .right_side {
                float: left;
                width: 700px;
                height: 1000px;
                border: 1px solid red;
                margin-left: 50px;
            }

            ```
          + 참고 - https://victorydntmd.tistory.com/187
          
      + 개선 사항
        + div 태그 내에서 p태그 가로 세로 가운데 정렬 하는 방법
        

## 12월 27일

+ 잘 된 부분
  + 카테고리 상세 페이지 레이아웃 수정
    + 컨텐트 영역에 left_side div 와 right_side div 추가
      + float을 사용하여 left 정렬후 margin-left 속성을 사용하여 여백 줌
      + ul li 태그를 사용하여 내비게이션 바를 만들어봄
        + ```
                    <ul>
                        <li class="dropdown1">
                            <div class="dropdown-menu1">HTTP</div>
                            <div class="dropdown-content1">
                                <a href="#">인터넷과 네트워크</a>
                            </div>
                        </li>
                    </ul>

                    <ul>
                        <li class="dropdown2">
                            <div class="dropdown-menu2">
                                프론트엔드
                            </div>
                            <div class="dropdown-content2">
                                <a href="#">HTML</a>
                                <a href="#">CSS</a>
                            </div>
                        </li>
                    </ul>


          ```
        + 참고 - https://dinfree.com/lecture/frontend/122_css_proj.html
      
      + table 태그를 사용하여 table 생성
        + ```
                 <table border="2">
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>Title</th>
                            <th>댓글수</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>title1</td>
                            <td>(10)</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>title2</td>
                            <td>(5)</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>title3</td>
                            <td>(3)</td>
                        </tr>
                    </tbody>
                </table>
          ```
          + 참고 - https://www.codingfactory.net/10510

        + div를 사용하여 카드 레이아웃 생성
          +   ```
                 <div class="card-box">
                        <img src="images/login_image.png">
                        <div class="card-body">
                            <h5>card-title</h5>
                            <p>content</p>
                            <a href="#" type="button">상세보기</a>
                        </div>
                  </div>


              ```

          + 참고 - https://www.codingfactory.net/11458
    + 알게된 부분
      + li 태그에 앞에 점 없애기
        + list-style-type: none;
      + a 태그 밑줄 없애기
        + text-decoration-line: none;

    + 개선해야 하는 부분
      + 페이징 버튼 레이아웃 
        + 카드 레이아웃 한 줄에 몇개 오게 할지
      + 카드 레이아웃 모양


## 12월 28일
  + 메인페이지 레이아웃 수정
    + 잘된점 
      + float을 사용하여 header 레이아웃  배치
        +  ```
           div {
                box-sizing: border-box;
            }

            .blog_top {
                width: 1000px;
                height: 100px;
                border: 1px solid black;
                margin-left: 15%;
            }

            .blog_top .left_side {
                float: left;
                width: 100px;
                height: 50px;
                margin-left: 10px;
                border: 1px solid red;
                margin-top: 15px;

            }

             .right_side div {
                margin-left: 600px;
                float: left;
                border: 1px solid green;
                margin-top: 30px;
                
            }

            .right_side div button {
                margin-left: 10px;
                margin-top: 5px;
            }
           ```
        + div 내그 p 태그 정렬
          + p태그를 div로 한번 감싸서 정렬
            +  ```
                     .left_side .blog_title {
                        width: 80px;
                        height: 40px;
                        border: 1px solid orange;
                        margin-left: 20px;
                        margin-top: -6px;
                        
                    }

                    .blog_title p {
                        font-size: 1.25rem;
                    }
              ```


        + ul li를 사용하여 dropdownlist 구현
          +  ```
                 <ul>
                    <li class="dropdown">
                        <div class="dropdown-menu">HTTP</div>
                        <div class="dropdown-content">
                            <a href="#">인터넷과 네트워크</a>
                            <a href="#">URI와 웹 브라우저 요청흐름 (2)</a>
                            <a href="#">HTTP 기본</a>
                            <a href="#">HTTP 메서드</a>
                        </div>

                    </li>
                </ul>
             ```
            + dropdown : 각각의 메뉴를 구성하는 껍데기 클래스
            + dropdown-menu : 메인 메뉴 항목을 정의하는 클래스
            + dropdown-content : 서브메뉴가 있을 경우 드롭다운으로 나타난다
              + 서브 메뉴 목록 지정 클래스


        + div를 사용하여 card-box 만들기
          + ```
              <div class="card_box">
                  <div class="card_image">
                      <img src="images/login_image.png">
                  </div>
                  <div class="card_content">
                      <h3><a href="#">글 제목</a></h3>
                      <div>
                          <span>작성자</span> <span>작성일</span>
                      </div>
                      
                      <a href="#">대분류 카테고리</a> <a href="#">소분류 카테고리</a>
                      <div class="content">
                          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus, tempore. Dolorum vero sed in consectetur eos commodi animi incidunt optio id hic nesciunt ut, pariatur obcaecati veritatis officiis itaque deserunt.</p>
                      </div>
                  </div>
               </div>
         + div 를 사용하여 footer 만들기
            + ```
                <div class="blog_footer">
                  <div>
                      <p> DevLog.CMY <br>
                          <a href="#">@2021 DevLog.CMY</a><br>
                          Powered By CMY
                      </p>
                      
                  </div>
              </div>

              

            .blog_footer {
                display: inline-block;
                margin-left: 15%;
                margin-top: 20px;
                width: 1000px;
                height: 90px;
                border: 1px solid royalblue;
            }

            .blog_footer div {
                display: inline-block;
                text-align: center;
                margin-left: 50%;
               
            }

            ```

     + 개선해야 하는 부분
       + 페이지네이션 레이아웃 설계
       + 카테고리 상세 페이지 
        + 레이아웃 , 헤더 , footer
       + 글 상세 페이지
         + 레이아웃
           + 가로 3개 div 레이아웃 으로 변경
           + 1:1 채팅 버튼 추가
           + 질문하기 버튼 추가
         + 헤더
         + footer
        










              


               

        

