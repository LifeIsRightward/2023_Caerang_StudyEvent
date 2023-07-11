<h1>드림코딩 4강(HTML정리)</h1>

드림코딩 4강

HTML의 구성요소
요소들(Elements)로 구성됨 -> 태그 한 쌍(+ 속성)으로 이루어짐 ex) <p>(시작태그) Hello World!(컨텐츠) </p>(종료태그) 이게 요소임 
<태그 속성1 = “속성값1”> 컨텐츠, 보이는 내용</태그>

중첩요소 가능 -> <p>Hello<strong>World</strong>!</p> 이런식으로
컨텐츠가 없는 태그도 있음  -> <img src = “image.png” alt = “profile”/>

HTML의 구조
<html> 
	<head> 
		// html 페이지에 대한 메타데이터(책 표지 같은 느낌), 웹 사이트에 대한 설명
	</head>
	<body>
		// 웹 사이트에 대한 내용(책 내용), UI
	</body> 
</html>

<!Document html> -> 이 파일의 문서 타입은 HTML5 이다. 라는걸 명시(관행적으로 무조건 작성해야하는 라인)
<html lang = “en”> -> 최상위 root 요소. / 속성이 하나 있는데, lang 속성: 문서에서 사용하는 주 언어 명시  / 속성 값: en 은 영어(English)
	<head> -> 문서의 메타데이터 + UI 상으로 보여지지 않는 정보들 / SEO(Search Engine Optimization 검색엔진 최적화 - 타이틀, 설명, 저자) + CSS스타일 / JS링크 등
		<meta charset = “UTF-8”/> -> charset(문자열 세트): UTF-8(다양한 언어를 깨짐 현상 없이 나타냄.) 인코딩 / meta 태그를 사용해서 다양한 속성을 지정할 수 있음
		<meta http-equip = “X-UA-Compatible(IE9 주소바에 호환성 버튼 안보이게)” content = “IE=edge(Edge 렌더링 엔진 사용)” /> -> IE 브라우저를 위한 설정
		<meta name = “viewport” content = “width=device-width, initial-scale= 1.0” /> -> viewport에 관련된 설정 / 사용자의 디바이스(viewport) 크기에 맞게 컨텐츠 표기
		<title>Document</title> -> 웹 사이트의 제목
	</head>
	<body> -> 문서의 UI 구성 요소들(사용자에게 보여지는)
		//구조적인 텍스트는 제목, 부제목, 단락 으로 구성되어 있음 -> 그래야 시각적으로 한 눈에 파악이 가능
	</body>
</html>

HTML을 작성할때, 전부 div로 작성하는거 보다 -> HTML5의 구조적인 태그들 즉, 시멘틱 태그를 사용하는것이 좋음.
￼￼

1. Element 레벨 vs container 레벨
	Element -> h1 ~ h6 , adress, blockquote, p, pre, table, il, ul, a, abbr, audio, b, span, cite, code, data, I, mark
	Container(요소들을 담을수있는 컨테이너요소) -> div, section, article, header, footer, aside, nav, main

￼
2. Block 레벨 vs inline 레벨
	Block -> 요소 하나당 한 줄을 꽉 차지함.
	h1~h6, address, block quote, p, pre, table, ol, ul
	Inline -> 그들의 컨텐츠만큼 자리를 차지함.
	a, abbr, audio, b, span, cite, code, data, I, mark
￼

유용한 웹 사이트 -> MDN(HTML, CSS, JS 에 대한 공홈느낌의 사이트임) https://developer.mozilla.org/ko/
https://html.spec.whatwg.org/ -> HTML 표준 규격(현업에 가면 많이 쓴다.)

웹 사이트 구조 분해(넷플릭스, 당근마켓) -> png 파일로 준게 있으니까 그걸 내가 스스로 분해해서 구조를 분해해봐라 ㅇㅇ 
시멘틱 태그를 잘 활용하라는 말씀인거 같음.

당근마켓

상단 -> 전반적인 링크 header 태그에 1. Div_logo 2. Nav태그 3. Div_input
중단 -> main태그
하단 -> footer 사이트에 대한 정보

그걸 바탕으로 한번 당근마켓을 분해해봤는데
￼￼￼
일단 나는 이런식으로 하긴했음 ㅇㅇ 정답은 없다니까,,, 걍 내가 하는게 정답이지 뭐 ㅋㅋ

개발자 도구(Mac의 경우에는 옵션 + 커맨드 + i)를 보면서 웹 사이트에 대한 정보를 읽어나갈 수 있음.
요소를 가져다가 대면 
오렌지색상 -> 마진
초록색 -> 패딩


