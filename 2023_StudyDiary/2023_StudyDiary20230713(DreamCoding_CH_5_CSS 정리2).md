<h1>드림코딩 5강 CSS 정리 2편</h1>


9.1 ~ 9.5 실습 -> 정렬파트
Magin: auto -> 블럭요소에 대한 수평정렬
.inner {
        width: 50%; 
          /* 200px의 50%(100px -> 자식의 컨텐츠의 너비만이 100px이라는 뜻임.) */
        height: 50%;
          /* 100px의 50%(50px -> 자식의 컨텐츠의 높이만이 50px이라는 뜻임.) */
        background-color: blue;
        margin: auto;
        /* 중간 배치(가운데 배치) -> 처음에 margin을 주지않고, 개발자도구로 확인해보면 inner클래스가 부모인 box클래스의 안에 속해있는데 오른쪽이 전부 마진으로
        자동적으로 빼곡하게 채워져있다. 이를 확인 후, 가운데 배치를 해주려면 margin: auto 를 사용한다. 그렇게 되면 좌, 우의 마진이 알아서 균등하게 설정(분배)되기때문에,
        컨텐츠는(보더를 포함한 컨텐츠) 가운데로 오게된다. */
        /* 블럭레벨의 경우에는 margin이 기본적으로 오른쪽에만 들어가게된다.(왜냐면 기본적인 flow가 왼쪽부터 시작하기 때문이다.) */
        /* 블럭레벨인 경우 균등하게 분배해서 수평으로 중간정렬을 하고싶으면, margin: auto;를 사용하면 된다. */

         /* 결론적으로 블럭레벨에서의 좌우 정렬을 하고싶을때 , margin: auto;를 주면됨. */
      }

Text-align -> 인라인요소에 대한 수평정렬
text-align: center;
        /* 이름이 텍스트 얼라인이라 텍스트만 정렬할거 같지만, 부모 컨테이너 안에 들어있는 인라인 요소들을 정렬할때도 사용함. */
        /* 결론적으로 인라인 레벨의 좌 우 정렬을 하고싶으면, text-align: center;로 하면된다. */

Line-height -> 텍스트 수직정렬
.box {
        width: 200px;
        height: 100px;
        background-color: grey;      
        /* 수평으로도 중간일 뿐만아니라, 수직으로도 중간으로 정렬하고싶음. */
        text-align: center;
        /* 이게 수평으로 정렬한거. */
      }
      .text{
        height: 100%;
        line-height: 100px;
        /* 텍스트 자체를 수직으로 부모를 가득 채워서 강제적으로 중간정렬 시켜주는 방법 -> text 의 height 을 부모의 100%로 맞춰주고 */
        /* text의 line-height: 라는 속성을 사용하여서 부모의 높이인 height: 을 100px로 맞춰주면은 중간정렬이 됨. -> 약간 편법같은 방법임 ㅇㅇ.*/
          /* 근복적으로 line-height 은 텍스트 줄의 간격을 조정할 수 있는 속성임. 그런데 부모의 높이만큼 간극을 주고 부모와 같은 너비가 되면, 가운데로 오게되니까
          편볍으로 정렬하는 방법인거지 ㅇㅇ 그래서 부모의 높이랑 같아야 정렬되는거임 line-height 는 ㅇㅇ */
          /* 얘 보다도 좋은 방법이 있대. 그게 flex인거지 ㅋㅋ */
      }

Transform: transition(); -> 기준점에 대해 이동

.inner {
        width: 80px;
        height: 80px;
        background-color: blue;
        /* 박스안에 또다른 자식(블럭요소인)요소가 있는데 이걸 중간으로 정렬할 수 있는방법이 -> translate */
        /* 여기서 innerbox를 기존의 자리를 유지할것인지, 안할것인지에 따라 사용하는 position의 속성값이 달라짐. */
        position: relative;
        /* 기존의 자리 유지 -> relative */
        top: 50%;
        /* 부모 높이 기준으로 50%만큼 아래로 이동. */
        left: 50%;
        /* 부모 너비 기준으로 50%만큼 오른쪽으로 이동. */
        transform: translate(-50%, -50%);
        /* 현재 나의 요소의 크기의(너비, 높이) 50%를 말함. */
        /* 잘 쓰이는 않음 ㅋㅋ */
      }


Display: Flex -> 플렉스 박스

.box {
        width: 200px;
        height: 200px;
        background-color: grey;
        display: flex; 
        /* 플렉스 컨테이너인거지 얘가(부모니까) 당연히 선언도 부모가 선언해줘야 컨테이너 아래에있는 플렉스 박스들. 즉, 자식들이 플렉스 박스라고 정의되는거임 ㅇㅇ */ 
        /* 그니까 너는 인제 플렉스 박스야. 라고 말해주는거임 */
        justify-content: center; 
        /* 기준축 정렬 -> 기준축은 디폴트가 row. 만약 flex-direction: column; 을 주게된다면 플렉스박스의 기준축이 수직이됨. */
        /* 일단 지금은 아무런 변경사항이 없으니 ,justify-content의 속성은 수평정렬임(지금은) */
        align-items: center;
        /* 기준축의 반대 정렬(반대축) -> 지금은 수직인거지. 기준축이 수평이니까 지금은 ㅇㅇ 수직정렬(지금은) */
      }

10 실습 -> 반응형(근데 미디어 쿼리를 사용하지 않음. 그냥 background 속성을 사용해서 반응형을 만듦.)
.box1{
        background-image: url('https://media.swncdn.com/cms/BST/67912-gettyimages-817147678-kieferpix.1200w.tn.webp');
        background-repeat: no-repeat;
        /* 너비가 커져도 이미지가 반복되지 않음. */
        background-position: center;
        /* 이미지를 중간으로 오도록 배치해줌. */
        background-size: cover;
        /* 이미지를 조금 더 반응적으로 만들어줌 -> 웹 페이지의 크기가 커지고 줄어듦에 따라 이미지의 가운데를 기준으로 비율에 맞게 커지고, 작아짐. */
        /* background-size: contain; -> 얘는 웹 페이지가 커지고 줄어듦에 따라 작아지고 커지지 않음. 걍 그 크기를 유지함. */
      }

      .box2{
        background: center/cover no-repeat 
        url('https://media.swncdn.com/cms/BST/67912-gettyimages-817147678-kieferpix.1200w.tn.webp');
        /* box1의 내용을 한번에 함축해서 사용한게 box2의 css */
      }

      .box3{
        background: center/cover fixed 
        url('https://media.swncdn.com/cms/BST/67912-gettyimages-817147678-kieferpix.1200w.tn.webp');
      }
