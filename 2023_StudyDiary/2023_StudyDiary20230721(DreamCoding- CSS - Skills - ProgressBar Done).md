/* Global */
:root{
    /* App Colors */

    /* 색깔보다 한 단계 더 추상적으로 사용하는 색깔들인거암. 웹의 전반적인 색깔을 담당하는
    primary, 강조할때 사용하는 accent, 그리고 텍스트의 색깔인 text까지 이렇게 내가 CSS내에서
    사용하는 색깔조차도 나중에 변수로 만들어서 사용가능하다는것이다. */
    --color-primary: var(--color-black);
    --color-primary-variant: var(--color-gray);
    /* 주로 사용하는 프라이머리 색상에 대한 변형을 하나 더 정의.(프라이머리 하나만 사용하면 밋밋하니까~) */
    --color-accent: var(--color-blue);
    --color-accent-variant: var(--color-orange);
    /* 얘도 같은 의미에서 베리언트를 설정해줌. 액센트 색깔 하나만 사용하면 밋밋하니까 ㅇㅇ */
    --color-text: var(--color-white);
    
    /* Colors */
    --color-white: #ffffff;
    --color-black: #050a13;
    --color-blue: #03e8f9;
    --color-orange: #fd6413;
    --color-gray: #1b1e26;

    /* Size */
    --size-max-width: 1200px;
}

*{
    box-sizing: border-box;
    /* 조금 더 직관적으로 너비와 높이를 명시할 수 있도록(패딩과 보더까지 합해서 위드와 하이트가 지정될 수 있도록 하기 위함) */
}

body{
    font-family: 'Noto Sans KR', sans-serif;
    margin: 0;
}

h1, h2, h3, p, ul{
    margin: 0;
}

ul{
    list-style: none;
    padding: 0;
}

a{
    text-decoration: none;
    color: var(--color-text);
}

button{
    background-color: transparent;
    outline: 0;
    border: 0;
}

button:focus{
    outline: 1px solid var(--color-accent);
}
/* Common(재사용 목적 css, 흐름이 비슷한 것들한테는 공통적인 스타일링을 해줌.) */
.section{
    padding: 4rem;
    text-align: center;
}

.title{
    font-size: 2.5rem;
    margin: 1rem 0;
}

.description{
    font-size: 1.5rem;
    margin: 0.5rem 0;
}

.max-container{
    max-width: var(--size-max-width);
    margin: auto;
}

/* Header */
.header{
    background-color: #050a13;
    position: fixed;
    top: 0;
    width: 100%;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    /* flex에서 기준축(지금은 수평)에 대한 정렬 속성값은 정렬하는 방식에 따라 상이함. */
    align-items: center;
    /* flex에서 기준축의 반대축(지금에서 반대축은 수직)에 대한 정렬 속성값은 정렬하는 방식에 따라 상이함. */
}

.header__logo{
    display: flex;
    align-items: center;
    gap: 8px;
    /* flex 박스 안에들어있는 자식들간의 여백(gap)을 관리*/
}

.header__logo__img{
    width: 36px;
    height: 36px;
}

.header__logo__title{
    font-size: 1.8rem;
    /* rem은 상대적인 유닛. 현재 브라우저에 설정되어있는 폰트 사이즈에 1.8배임 */
}

.header__menu{
    display: flex;
    gap: 4px;
}

.header__menu__item{
    padding: 8px 16px;
    margin-left: 16px;
}

.header__menu__item:hover{
    border-bottom: 2px solid var(--color-accent);
}
/* 클래스 두개를 선택하려면(같은 태그 안에서) 붙혀서 써야함. */
.header__menu__item.active{
    border: 1px solid var(--color-accent);
    border-radius: 4px;
}

/* Home */
#home{
    background-color: var(--color-primary);
    color: var(--color-text);
    padding: 5rem 1rem;
    padding-top: 7rem;
    text-align: center;
}

.home__avatar{
    width: 250px;
    height: 250px;
    object-fit: cover;
    /* 이미지의 원래 비율이 유지됨. 위드와 하이트에 상관없이 유지됨 */
    border: 3px solid var(--color-accent);
    border-radius: 100%;
}

.home__title{
    font-size: 3rem;
    margin-bottom: 1rem;
}

.home__title--strong{
    color: var(--color-accent);
}

.home__description{
    font-size: 1.3rem;
}

.home__contact{
    display: inline-block;
    color: var(--color-black);
    background-color: var(--color-accent);
    padding: 0.5rem, 1rem;
    margin: 2rem;
    font-weight: bold;
    border-radius: 4px;
}

.home__contact:hover{
    background-color: transparent;
    color: var(--color-text);
    outline: 2px solid var(--color-accent);
    /* 보더로 하면 박스 사이징 속성때문에 버튼이 호버될때 컨텐츠들이 밀려나면서 안이뻐진다. -> 그래서 보더말고 아웃라인으로 해준거임 ㅇㅇ */
}

/* About */
.majors{
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    margin: 2.5rem 0;
}

.major{
    background-color: var(--color-primary-variant);
    padding: 2rem 1rem;
    color: var(--color-text);
    border-radius: 1rem;
    cursor: default;
    box-shadow: 4.0px 8.0px 8.0px rgba(0,0,0,0.38);
}

.major__icon{
    font-size: 4rem;
    margin: 1rem 0;
    color: var(--color-accent);
    transition: all 350ms ease;
}

.major__title{
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 1rem;
}

.major:hover .major__icon{
    transform: rotate(-15deg) scale(1.2);
}

.jobs{
    text-align: start;
}

.jobs{
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 1rem;
}

.job__name{
    color: var(--color-primary);
}

.job__perioid{
    color: var(--color-primary);
    font-size: 0.8rem;
}

/* Skills */
/* skills라는 섹션을 아이디로 정해놨기에 아이디 선택자를 사용. */
#skills{
    background-color: var(--color-primary-variant);
    color: var(--color-text);
}

.skills{
    display: grid;
    /* 넌 이제 그리드 박스야 */
    grid-template-columns: 6fr 4fr;
    /* 그리드는 총 2개의 행이 있는데, 각각 6배 4배로 반들어줄거임. */
    margin: 2rem 3rem;
    border-radius: 8px;
    /* 보더 래디우스를 줘도 각져있다. 그 이유는  우리가 그리드라는 컨테이너 자체에는 
    보더 래디우스가 적용되어있지만, 그 안에 들어있는 스킬즈 코딩(클래스) 자체가 백그라운드 색상이 프라이머리 색상으로 지정되어있어서 그리드 밖으로 삐져나와서 프라이머리 색상이 보이는거임.*/
    overflow: hidden;
    /* 그래서 스킬즈에게 보더 래디우스가 이건데, 혹시나 내 자식요소중에 내 컨테이너 밖으로 나온애가 있다면 보이지 않게 overflow: hiddend을 해준거임.*/

    box-shadow: 0 2.8px 2.2px rgba(0, 0, 0, 0.034), 0 6.7px 5.3px rgba(0, 0, 0, 0.048), 0 12.5px 10px rgba(0, 0, 0, 0.06), 0 22.3px 17.9px rgba(0, 0, 0, 0.072), 0 41.8px 33.4px rgba(0, 0, 0, 0.086), 0 100px 80px rgba(0, 0, 0, 0.12)
}

.skills__title{
    color: var(--color-accent);
    margin: 1rem 0;
    font-size: 1.2rem;
}

.skills__coding{
    grid-row: span 2;
    padding: 1rem;
    background-color: var(--color-primary);
}

.skills__tools{
    padding: 1rem;
}

.skills__etc{
    padding: 1rem;
    background-color: var(--color-primary);
    filter: brightness(150%);
    /* 동일한 색깔을 쓰더라도 다르게 표현하고싶으면, 필터를 사용하면됨. 
    필터 중에서도 조금 더 밝게 해주는 brightness를 사용했음. */
    /* 웹 사이트에서 사용하는 코드를 많이 만들지 않더라도, 필터를 통해서 다른 느낌의 연출을 진행할 수 있음. */
}

/* Skills의 Progress Bar */

.bar{
    display: flex;
    flex-direction: column;
    padding: 1rem;
    gap: 0.5rem;
}

.bar__metadata{
    display: flex;
    justify-content: space-between;
}

.bar__bg{
    width: 100%;
    height: 3px;
    background-color: var(--color-primary-variant);
}

.bar__value{
    height: 3px;
    background-color: var(--color-accent);
}
