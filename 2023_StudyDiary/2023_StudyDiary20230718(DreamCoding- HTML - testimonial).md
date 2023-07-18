<h1>HTML 개발 1편</h1>

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- SEO(Search Engine Optimization)  검색엔진최적화.-->
    <!-- 검색자(검색 유저)의 의도를 이해하고 이에 충실히 맞춰 웹 페이지의 콘텐츠를 제작하고, 이 페이지가검색 결과 페이지에서 잘 노출 되도록
    웹 페이지의 태그와 링크 구조를 개선하여 자연 유입 트래픽을 늘리는 시책이라고 할 수 있다.-->
    <title>DaeHyun&#39;s PortFolio</title>
    <!-- 어커스트로피 s를 쓰고싶은데 그게 태그로 오해될까봐 이스케이프 문자를 써준거임 " ' " 이거 말하는거 -> &#39 이거임.-->
    <meta name="description" content="PortFolio for World-renowned Software enginner DaeHyun">
    <meta name="author" content="DaeHyun">
    <link rel="shortcut icon" href="images/profile.jpg" type="image/x-icon">
    <!-- favicon(북마크나 웹페이지 왼쪽 상단에 작은 아이콘 같은거 그걸 '페비콘'이라고 하나봐...)이 왜 안될까,..? 근데 ico 확장자는 안되고, jpg 확장자는 되네..?-->
    <!-- OG(Open Graph Data) -->
    <!-- 쉽게 말해 사이트를 공유했을 때, 사이트를 접속하기 이전에도 사이트에 대한 정보를 '미리' 확인해 볼 수 있는 미리보기와 같은 뜻이다.' -->
    <meta property="og:title" content="대현이의 포트폴리오">
    <meta property="og:type" content="website">
    <meta property="og:url" content="배포후 생성된 URL">
    <meta property="og:image" content="배포후 생성된 이미지 URL ">
    <!-- Goggle Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <script src="https://kit.fontawesome.com/86c243af6d.js" crossorigin="anonymous"></script>
    <!-- CSS -->
    <link rel="stylesheet" href="css/style.css">
    <!-- Java Script -->
    <script src="src/main.js" defer></script>
</head>
<body>
    <!-- Header -->
    <header>
        <div>
            <img src="images/favicon.ico" alt="logo">
            <h1><a href="#">DaeHyun</a></h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#work">My work</a></li>
                <li><a href="#testimonial">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <!-- Main -->
    <main>
        <!-- Home -->
        <section id="home">
            <img src="images/profile.jpg" alt="DaeHyun's profile">
            <h2>Hello I&#39;m Dream Coder, DaeHyun</h2>
            <p>Software Enginner residing in Seoul, Republic of South Korea</p>
            <a href="#contact">Contaact Me</a>
        </section>
        <!-- About -->
        <section id="about">
            <h2>About me</h2>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. 
                Quidem minus labore excepturi, molestias ea laudantium dolor fuga 
                quod modi deserunt dolorum temporibus hic numquam delectus 
                vitae nostrum nobis accusamus beatae.
            </p>
            <ul>
                <li>
                    <i class="fa-brands fa-html5"></i>
                    <p>Front-End</p>
                    <p>HTML, CSS, JavaScript, TypeScript, React, Vue, Web APIs</p>
                </li>
                <li>
                    <i class="fa-solid fa-mobile"></i>
                    <p>Moblie</p>
                    <p>Android, iOS, React Native, Flutter, Java, Swift, Kotlin</p>
                </li>
                <li>
                    <i class="fa-solid fa-server"></i>
                    <p>Back-End</p>
                    <p>Java, JavaScript, Go, NodeJS, Rest APIs, GraphQL</p>
                </li>
            </ul>
            <ul>
                <li>
                    <img src="images/HallymLogo.png" alt="Hallym Logo">
                    <div>
                        <p>Hallyym Univ as Student</p>
                        <p>2019 Feb - Untill now</p>
                    </div>
                </li>
                <li>
                    <img src="images/YMLogo.png" alt="YM Logo">
                    <div>
                        <p>YongMoon High as Student</p>
                        <p>2016 Feb - 2019 Feb</p>
                    </div>
                </li>
            </ul>
        </section>
        <!-- Skills -->
        <section id="skills">
            <h2>My Skills</h2>
            <p>Skills & Atributes</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Minus, voluptatem magnam quae quasi tenetur saepe exercitationem,
                excepturi nihil esse eos vitae voluptates sint cupiditate quisquam 
                eum sequi blanditiis laborum. Deserunt.
            </p>
            <div>
                <section>
                    <h3>Coding Skills</h3>
                    <ul>
                        <li>
                            <div><span>HTML</span><span>98%</span></div>
                            <div><div style="width: 98%"></div></div>
                        </li>
                        <li>
                            <div><span>CSS</span><span>90%</span></div>
                            <div><div style="width: 90%"></div></div>
                        </li>
                        <li>
                            <div><span>JavaScript</span><span>90%</span></div>
                            <div><div style="width: 98%"></div></div>
                        </li>
                        <li>
                            <div><span>TypeScript</span><span>80%</span></div>
                            <div><div style="width: 98%"></div></div>
                        </li>
                        <li>
                            <div><span>React</span><span>77%%</span></div>
                            <div><div style="width: 98%"></div></div>
                        </li>
                        <li>
                            <div><span>NodeJS</span><span>68%</span></div>
                            <div><div style="width: 98%"></div></div>
                        </li>
                    </ul>
                </section>
                <section>
                    <h3>Tools</h3>
                    <ul>
                        <li>Visual Studio Code</li>
                        <li>IntelliJ</li>
                        <li>Android Studio</li>
                        <li>iOS development tools</li>
                        <li>Figma</li>
                    </ul>
                </section>
                <section>
                    <h3>Etc</h3>
                    <ul>
                        <li>Git</li>
                        <li>Scrum Master</li>
                        <li>Math</li>
                    </ul>
                </section>
            </div>
        </section>
        <!-- Work -->
        <section id="work">
            <h2>My Work</h2>
            <p>Projects</p>
            <ul>
                <li><button>ALL <span>8</span></button></li>
                <li><button>Front-End</button><span>3</span></li>
                <li><button>Back-End</button><span>3</span></li>
                <li><button>Moblie</button><span>2</span></li>
            </ul>
            <ul>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project1.webp" alt="project1">
                    <div>
                        <h3>Project #1</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project2.webp" alt="project2">
                    <div>
                        <h3>Project #2</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project3.webp" alt="project3">
                    <div>
                        <h3>Project #3</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project4.webp" alt="project4">
                    <div>
                        <h3>Project #4</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project5.webp" alt="project5">
                    <div>
                        <h3>Project #5</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project6.webp" alt="project6">
                    <div>
                        <h3>Project #6</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project7.webp" alt="project7">
                    <div>
                        <h3>Project #7</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
                <li><a href="#" target="_blank">
                    <img src="images/projects/project8.webp" alt="project8">
                    <div>
                        <h3>Project #8</h3>
                        <p>Colone Coding with HTML, CSS</p>
                    </div>
                </a></li>
            </ul>
        </section>
        <!-- Testimonials -->
        <section id="testimonial">
            <h2>Testimonial</h2>
            <p>See Waht They Say About Me</p>
            <ul>
                <li>
                    <img src="images/testimonials/people1.webp" alt="people1">
                    <div>
                        <p>
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                            Molestias optio totam, a facere dolore reprehenderit voluptate libero porro voluptas 
                            distinctio amet cupiditate quisquam doloribus accusantium doloremque modi architecto, itaque cumque.
                        </p>
                        <p><a href="#">James Kim</a> / Google</p>
                    </div>
                </li>
                <li>
                    <img src="images/testimonials/people2.webp" alt="people2">
                    <div>
                        <p>
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                            Molestias optio totam, a facere dolore reprehenderit voluptate libero porro voluptas 
                            distinctio amet cupiditate quisquam doloribus accusantium doloremque modi architecto, itaque cumque.
                        </p>
                        <p><a href="#">Anna Jin</a> / Samsung</p>
                    </div>
                </li>
                <li>
                    <img src="images/testimonials/people3.webp" alt="people3">
                    <div>
                        <p>
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                            Molestias optio totam, a facere dolore reprehenderit voluptate libero porro voluptas 
                            distinctio amet cupiditate quisquam doloribus accusantium doloremque modi architecto, itaque cumque.
                        </p>
                        <p><a href="#">Yerim Yeon</a> / Amazon</p>
                    </div>
                </li>
            </ul>
        </section>
        <!-- Arrow Up(오른쪽 하단에 화살표 모양 업 표시) -->
        <aside></aside>
    </main>
    <!-- Footer -->
    <footer id="contact"></footer> 
</body>
</html>
