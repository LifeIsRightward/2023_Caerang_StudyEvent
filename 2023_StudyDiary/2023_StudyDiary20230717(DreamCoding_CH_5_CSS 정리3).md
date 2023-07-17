<h1>드림코딩 5강 CSS 정리 3편</h1>
11 실습 -> 트랜스폼(좌표, 위치, 각도, 크기 조정)
 .box {
        width: 100px;
        height: 120px;
        background-color: brown;
        margin-bottom: 20px;
      }

      /* transform 자체가 -> a에서 b로 형태를 바꾸어 나가는것 */
      .box1{
        transform: translateX(100px);
        /* 얘는 x의 좌표만 100px 움직임.(현재 위치에서) 양수값이면 우측으로 이동, 음수값이면 좌측으로이동. (X좌표를 움직일때는 ㅇㅇ) */
      }
      .box2{
        transform: translate(-50px, -20px);
        /* 얘는 x의 좌표를 -50px, y의 좌표를 -20px을 움직인다. 즉 왼쪽으로 50px 아래로 20px 움직이게 한다. */
      }
      .box3{
        transform: scale(1.2);
        /* 1.2배로 키운다는 뜻임 */
        /* transform은 좌표를 이동시키는것 뿐만 아니라, 크기 자체를 변경시킬수도 있음 -> scale */
      }
      .box4{
        transform: rotate(45deg);
        /* 45도 각도롤 회전 */
      }
      .box5{
        transform: translate(100px, 100px) scale(2) rotate(15deg);
        /* 이렇게 한번에 사용할수도있음 */
      }



12 실습 -> 트랜지션(스무스한 동적 효과, 이벤트)
.box {
        width: 100px;
        height: 100px;
        margin: 20px;
        background-color: pink;
        /* transition: background-color 300ms linear; */
        transition: all 500ms linear;
        /* 그래서 이건 내가 바뀌는 모든것(속성)들에 대해서 트랜지션을 먹이고싶으면, transition: all을 쓰면됨 */
        /* linear 이런거가 "트랜지션 타이밍 펑션" 이라고 하는데, 일정한속도, 이지 등등이 있는다.
        별도로 설정하지않으면 디폴트는 이지로 설정됨. -> MDN 찾아보셈*/
        /* https://cubic-bezier.com/#.17,.67,.83,.67 여기 싸이트가 트랜지션 타이밍 펑션에 대해 눈으로 보기 쉽게
        해놓은 싸이트임. 참고하면 좋을듯 */
      }
      .box1:hover{
        background-color: blueviolet;
        /* 얘만 쓰면 급하게 호버 이벤트가 먹게되는데. 그거보다 은은하게 혹은 자연스럽게 먹이기 위해 트랜지션을 씀. */
        /* transition: background-color 300ms linear; */
        /* background-color 속성을 트랜지션을 할건데, 300ms동안에 핑크에서 보라색으로 변경. 어떤속도로할거냐 -> linear */
      }
        /* 근데 얘는 호버될때만 주는거라, 마우스를 내리면 다시 급격하게 색깔이 꺼지는데. 그거는 호버에 주는게 아니라 전체에 줘야 바뀜. */
      .box2:hover{
        border-radius: 100%;
        /* 100% -> 동그래짐. */
        background-color: cornflowerblue;
        /* 트랜지션은, 내가 지정한 속성에 대해서만 값이 먹힘. 즉, 컬러는 은은하게 바뀌지만, 보더 래디우스는 급격하게 바뀜
        그 이유가 바로 내가 트랜지션을 준 대상 속성이 백그라운드 컬러이기 때문인거지 ㅇㅇ */
      }
      .box3:hover{
        border-radius: 50%;
        transform: translate(400px);
        background-color: blue;
        /* 엄청 신기하게 움직임. */
        /* 마우스가 올라올때만 위치가 변경되기때문에, 마우스가 올라오면 오른쪽으로 요소가 가니까 자동으로 호버이벤트가 끝나면서
        다시 요소가 제자리로 돌아오게됨. */
      }


13 실습 -> 키 프레임(CSS에서 키프레임을 사용하면, 조금 더 정료한 애니메이션을 정의 할 수 있음.)
/* css에서 키프레임을 사용하면, 조금더 정교한 애니메이션을 정의할 수 있음 */
      @keyframes slidein{
        0%{
          border-radius: 0%;
          background-color: aquamarine;
        }
        /* 애니메이션이 시작할때 */
        50%{
          background-color: pink;
        }
        /* 애니메이션 중간때 */
        100%{
          border-radius: 100%;
          background-color: hotpink;
        }
        /* 애니메이션이 끝날때 */
      }
      .box {
        width: 100px;
        height: 100px;
        margin: 20px;
        background-color: chocolate;
        animation: 1500ms infinite alternate slidein;
        /* animation -> 이게 키프레임을 사용하기위한 속성. 몇 초동안, 내가 정의한 키프레임(애니메이션) 이런식으로
        만약 무한정으로 지속하고싶다면 infinite속성 사용 */
        /* alternate는 원래는 0% -> 50% -> 100% 하고 다시 0% -> 50% -> 100% 이렇게 하는데(infinite 속성 때문에)
        (이렇게 되면 마지막에 0%로 돌아올때 부자연스러워짐.)
        그런데 alternate를 사용하면, 0% -> 50% -> 100% -> 50% -> 0%로 자연스럽게 돌아가도록 설정해준다. */
      }

14 실습 -> CSS 변수 사용
:root{
        --background-color:darkslategrey;
        /* 루트에다가 정의. 더블 하이폰으로 시작 */
        --text-color: whitesmoke;
      }
      .first-list {
        background-color: var(--background-color);
        color: var(--text-color);
        margin-left: 8px;
      }
      .second-list {
        background-color: var(--background-color);
        color: var(--text-color);
        margin-left: 16px;
      }

      @media screen and (max-width: 768px){
          :root{
            --background-color:darkslateblue;
            /* 루트에다가 정의. 더블 하이폰으로 시작 */
            --text-color: white;
        }
      }

15실습 -> HTML 데이터(HTML에서의 변수 활용)

<style>
      div {
        width: 100px;
        height: 100px;
        background-color: tomato;
        margin-bottom: 50px;
      }

      div[data-display-name='dream']{
        background-color: beige;
      }
    </style>
  </head>
  <body>
    <!-- <img src="/images/profile.png" alt="대체 텍스트"/> -->
    <!-- alt는 이미지 경로가 보여지지않을때, 대체해서 보여주는거임 -->
    <!-- 우리가 자체적으로 이 태그에는 이 데이터값을 저장하고 싶다! 할때 쓰는게 data임. -->
    <!-- 사용 방식은 data-"원하는 속성의 키"="값" -->
    <!-- data-"사용할 데이터 변수이름" = "값" 이런식으로 사용하면됨. -->
    <div data-index = "1" data-display-name = "dream">드림!!</div>
    <div data-index = "2" data-display-name = "coding"></div>
    <span data-index= "1" data-display-name= "dream">드림!!</span>
    
    <script>
        const dream = document.querySelector('div[data-display-name="dream"]');
        console.log(dream.dataset);
        console.log(dream.dataset.displayName);
    </script>
