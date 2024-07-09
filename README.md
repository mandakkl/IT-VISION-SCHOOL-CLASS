# IT-VISION-SCHOOL-CLASS
## 포트폴리오 html코드
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/reset-css@5.0.2/reset.min.css" rel="stylesheet">
    <link rel="stylesheet" href="./css/main.css">
</head>
<body>
    <header>
        <div class="inner">
            <div class="logo">본인 이니셜</div>
            <div class="menu-toggle" id="menu-toggle">&#9776;</div>

            <ul class="nav-links" id="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>
    <!-- about -->
    <div class="about" id="about">
        <div class="about_contain" id="about_contain">
            <div class="about_wrap">
                <div class="img_wrap about_imgany" id="about_imgany">
                    <img src="./images/pic.jpg" alt="3d 얼굴사진">
                </div>
                <div class="about_name about_nameany" id="about_name">
                    본인 이름
                </div>
                <p class="about_job about_jobany" id="about_job"> Wep Developer</p>
                <div class="about_text">
                    This is my portfolio site.<br>
                    Please look around and contact me if you like it.
                </div>
            </div>
        </div>
    </div>
    <!-- skills -->
    <div class="skills inner" id="skills">
        <div class="title">Skills</div>
        <p>HTML, CSS, JS, 3D, Photoshop, Illustrator <br>
            I can work using various programs.</p>

            <div class="skill">
                <div class="skill_name">HTMl</div>
                <div class="skill_bar">
                    <div class="skill_per" per="90%" style="max-width: 90%; background-color: rgb(252, 92, 92);"></div>
                </div>
            </div>
    
            <div class="skill">
                <div class="skill_name">CSS</div>
                <div class="skill_bar">
                    <div class="skill_per" per="90%" style="max-width: 90%; background-color: rgb(255, 183, 111);"></div>
                </div>
            </div>
    
            <div class="skill">
                <div class="skill_name">JS</div>
                <div class="skill_bar">
                    <div class="skill_per" per="80%" style="max-width: 80%; background-color: rgb(91, 255, 140);"></div>
                </div>
            </div>
    
            <div class="skill">
                <div class="skill_name">3D</div>
                <div class="skill_bar">
                    <div class="skill_per" per="90%" style="max-width: 90%; background-color: rgb(106, 125, 255);"></div>
                </div>
            </div>
           
            <div class="skill">
                <div class="skill_name">Photoshop</div>
                <div class="skill_bar">
                    <div class="skill_per" per="100%" style="max-width: 100%; background-color: rgb(209, 91, 255);"></div>
                </div>
            </div>

            <div class="skill">
                <div class="skill_name">Illustrator</div>
                <div class="skill_bar">
                    <div class="skill_per" per="100%" style="max-width: 100%; background-color: rgb(255, 91, 151);"></div>
                </div>
            </div>
         
    </div>
    <!-- portfolio -->
    <div class="portfolio" id="portfolio"></div>
    <!-- contact -->
    <div class="contact" id="contact"></div>
    <!-- js -->
     <script src="./js/main.js"></script>
</body>
</html>
```
## 포트폴리오 css코드
```css
@import url('https://fonts.googleapis.com/css2?family=Alfa+Slab+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100..900&display=swap');

/* common */
html,
body{
    height: 100%;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
*{
    text-decoration: none;
}
.inner{
    width: 1100px;
    margin: 0 auto;
}
@media(max-width:768px){
    .inner{
        width: 90%;
    }
}

/* header */
header{
    background-color: #333;
    height: 70px;
    color: #fff;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    align-items: center;
    z-index: 10;
}
header .inner{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    max-width: 1100px;
    position: relative;
}
.logo{
    font-family: "Alfa Slab One", serif;
    font-weight: 400;
    font-style: normal;
}
.menu-toggle{
    font-size: 30px;
    cursor: pointer;
    display: none;
}
header .inner ul{
    display: flex;
}
header .inner ul > li{
    margin-left: 20px;
}
header .inner ul > li > a{
    color: #fff;
}
header .inner ul > li > a:hover{
    color:#0bf7ff;
    cursor: pointer;
}
@media(max-width:1024px){
    .logo{
        padding-left: 10px;
    }
    .nav-links{
        padding-right: 10px;
    }
}
@media(max-width:768px){
    header{
        height: 50px;
    }
    .logo{
        line-height: 50px;
        padding-left: 10px;
    }
    .menu-toggle{
        display: block;
        padding-right: 10px;
    }
    .nav-links{
        display: none;
        flex-direction: column;
        position: absolute;
        background-color: #1c1c1c;
        width: 100%;
        top: 50px;
        transition: max-height 0.3s ease-in-out;
        overflow: hidden;
        max-height: 0;
    }
    .nav-links.show{
        max-height: 300px;
    }
    header .inner ul{
        flex-direction: column;
        align-items: center;
    }
    .nav-links li{
        padding: 20px 0;
    }
}

/* about */
.about{
    height: 1000px;
    overflow-x:hidden;
}
.about #about_contain{
    width: 100%;
    height: 100%;
    background-color: rgb(0, 132, 255);
}
.about_wrap{
    position: relative;
    top: 300px;
    text-align: center;
}
.img_wrap{
    width: 250px;
    height: 250px;
    overflow: hidden;
    border-radius: 100%;
    margin: 0 auto;
    position: relative;
}


/* skills */
.skills{
    width: 100%;
    max-width: 900px;
    height: 1000px;
    background-color: rgb(255, 255, 255);
    overflow-x: hidden;
}
.skills .title{
    text-align: center;
    font-size: 45px;
    padding-top: 140px;
    font-family: "Noto Sans KR", sans-serif;
    font-optical-sizing: auto;
    font-weight: 600;
    font-style: normal;
}
.skills>p{
    text-align: center;
    font-size: 18px;
    line-height: 23px;
    padding-top: 10px;
    padding-bottom: 40px;
    font-family: "Noto Sans KR", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
}
.skill{
    padding: 0 40px;
}
.skill_name{
    font-size: 25px;
    font-weight: 700;
    color: #222;
    text-transform: uppercase;
    margin: 25px 0 5px 0;
}
.skill_bar{
    height: 35px;
    background-color: #c9c9c9;
    
}
.skill_per{
    height: 35px;
    color: #fff;
    font-weight: bold;
    position: relative;
    width: 100%;
    opacity: 0;
    transition: width 2.5s, opacity 2.5s;
}
.skill_per::before{
    content: attr(per);
    position: absolute;
    padding: 8px 10px;
    background-color: #222;
    border-radius: 4px;
    font-size: 20px;
    top: -50px;
    right: 0;
    transform: translateX(50%);
    opacity: 0;
    transition: opacity 2.5s;
    
}
.skill_per::after{
    content: "";
    position: absolute;
    width: 10px;
    height: 10px;
    background-color: #222;
    top: -20px;
    right: 0;
    transform: translateX(50%) rotate(45deg);
    border-radius: 2px;
    opacity: 0;
    transition: opacity 2.5s;
}
.skill_per.fillcolor {
    width: 100%;
    opacity: 1;
    animation: fillcolor 2s 1 forwards;
}
.skill_per.fillcolor::before,
.skill_per.fillcolor::after{
    opacity: 1;
}

@keyframes fillcolor{
    from{
        width: 0%;
    }
    to{
        width: 100%;
    }
}


@media(max-width:1024px){
    .skill{
        padding: 0 40px;
    }
}

@media(max-width:768px){
    .skill{
        padding: 0 40px;
    }
}
/* portfolio */
.portfolio{
    height: 1000px;
    background-color: rgb(208, 208, 208);
}
/* contact */
.contact{
    height: 1000px;
    background-color: rgb(20, 20, 20);
}
```
## 포트폴리오 js코드
```js


//모바일_toggle
document.addEventListener("DOMContentLoaded",function(){
    const header = document.querySelector("header");
    const navLinks = document.getElementById("nav-links");
    const menuToggle = document.getElementById("menu-toggle");
    const skillsSection = document.querySelector("#skills");
    let observer;

    function getHeaderHeight(){
        return header.offsetHeight;
    }

    menuToggle.addEventListener("click", function(){
        navLinks.classList.toggle("show");
    });
    
    //슬라이드
    document.querySelectorAll("header .inner ul li a").forEach(anchor => {
        anchor.addEventListener("click",function(e){
            e.preventDefault();
            const targetId = this.getAttribute("href").substring(1);
            const targetElement = document.getElementById(targetId);

            if(targetElement){
                window.scrollTo({
                    top: targetElement.offsetTop - getHeaderHeight(),
                    behavior: "smooth"
                });
                navLinks.classList.remove("show");

                 // Skills 섹션에 도달하면 애니메이션 시작
                 if (targetId === "skills") {
                    activateSkillBars();
                }
            }else{
                console.error(`Element with ID '${targetId}' not found.`);
            }
        });
    });

    window.addEventListener("resize", function(){
        getHeaderHeight();
    });

     // 페이지 로드 시 skills 섹션이 보이면 애니메이션 시작
     let skillPers = document.querySelectorAll(".skill_per");
     window.addEventListener('scroll', function() {
     let value = window.scrollY + window.innerHeight;
     let triggerPoint = document.querySelector("#skills").offsetTop + document.querySelector("#skills").offsetHeight * 0.93; // 애니메이션을 트리거할 위치 조정

     console.log("scrollY + window.innerHeight", value);
     console.log("triggerPoint", triggerPoint);

     if (value > triggerPoint) {
        skillPers.forEach(skillPer => {
            skillPer.classList.add('fillcolor');
        });
     }
});

    //skills bar 구동
    function activateSkillBars(){
        const skillElements = document.querySelectorAll('.skill_per');

        if(observer){
            observer.disconnect();
        }
        observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting){
                    skillElements.forEach(skill =>{
                        skill.classList.add('fillcolor');
                    });
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });

        skillElements.forEach(skill =>{
            skill.classList.remove('fillcolor');
        });
        observer.observe(skillsSection);
    }
});
```
## HTML, CSS를 활용한 움직이는 정육면체 만들기
### html코드
```html
<div class="cube">
    <div class="face front">앞면</div>
    <div class="face back">뒷면</div>
    <div class="face top">윗면</div>
    <div class="face bottom">바닥면</div>
    <div class="face left">왼쪽면</div>
    <div class="face right">오른쪽면</div>
</div>
```
### css코드
```css
.cube {
    padding-top: 400px;
    margin: 0 auto;
    width: 200px;
    height: 200px;
    position: relative;
    transform-style: preserve-3d;
    animation: rotateCube 5s infinite linear;
}

.face {
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgba(0, 0, 0, 0.3);
    border: 1px solid black;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 20px;
}

.front { transform: translateZ(100px); }
.back { transform: rotateY(180deg) translateZ(100px); }
.top { transform: rotateX(90deg) translateZ(100px); }
.bottom { transform: rotateX(-90deg) translateZ(100px); }
.left { transform: rotateY(-90deg) translateZ(100px); }
.right { transform: rotateY(90deg) translateZ(100px); }

@keyframes rotateCube {
    from { transform: rotateX(0deg) rotateY(0deg); }
    to { transform: rotateX(360deg) rotateY(360deg); }
}
```
## 디지털 시계 만들기
### html코드
```html
<div class="clock" id="clock">00:00:00</div>
```
### css코드
```css
html,body {
    height: 100%;
}
body{
    background: #0f3854;
    background: radial-gradient(ellipse at center, #0a2e38 0%, #000 70%);
    background-size: 100%;
  
}
#clock{
    color: #daf6ff;
    font-family: "Jersey 20", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 200px;
    text-align: center;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    text-shadow: 0 0 20px rgba(10, 175, 230, 1),  0 0 20px rgba(10, 175, 230, 0);
}
```
### js코드
```js
function updateClock() {
    var now = new Date();
    var hours = now.getHours();
    var minutes = now.getMinutes();
    var seconds = now.getSeconds();

    // 시, 분, 초가 한 자리 숫자일 경우 앞에 0을 붙여줍니다.
    hours = (hours < 10) ? '0' + hours : hours;
    minutes = (minutes < 10) ? '0' + minutes : minutes;
    seconds = (seconds < 10) ? '0' + seconds : seconds;

    // 시계 업데이트
    var clock = document.getElementById('clock');
    clock.textContent = hours + ':' + minutes + ':' + seconds;
}

// 1초마다 시계 업데이트
setInterval(updateClock, 1000);
```
## 계산기 만들기
### html코드
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>계산기</title>
    <link rel="stylesheet" href="./css/main.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button onclick="appendNumber('1')">1</button>
            <button onclick="appendNumber('2')">2</button>
            <button onclick="appendNumber('3')">3</button>
            <button onclick="performOperation('+')">+</button>
            <button onclick="appendNumber('4')">4</button>
            <button onclick="appendNumber('5')">5</button>
            <button onclick="appendNumber('6')">6</button>
            <button onclick="performOperation('-')">-</button>
            <button onclick="appendNumber('7')">7</button>
            <button onclick="appendNumber('8')">8</button>
            <button onclick="appendNumber('9')">9</button>
            <button onclick="performOperation('*')">*</button>
            <button onclick="appendNumber('0')">0</button>
            <button onclick="clearDisplay()">C</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="performOperation('/')">/</button>
        </div>
    </div>
    <script src="./js/main.js"></script>
</body>
</html>
```
### css코드
```css
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
body{
    background-color: rgb(59, 10, 133);
}
.calculator {
    background-color: rgb(147, 91, 152);
    width: 430px;
    margin: 50px auto;
    margin-top: 200px;
    padding: 20px;
    border: 1px solid #1d0541;
    border-radius: 5px;
}

input#display {
    background-color: rgb(29, 23, 32);
    width: 95%;
    height: 100px;
    margin-bottom: 10px;
    text-align: right;
    font-size: 50px;
    padding: 5px;
    color: white;
}

.buttons button {
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
    background: rgb(189, 155, 249);
    width: 100px;
    height: 100px;
    margin: 2px;
    font-size: 40px;
    cursor: pointer;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
}
```
### js코드
```js
let display = document.getElementById('display');

function appendNumber(number) {
    display.value += number;
}

function performOperation(operator) {
    display.value += operator;
}

function clearDisplay() {
    display.value = '';
}

function calculateResult() {
    try {
        display.value = eval(display.value);
    } catch (e) {
        display.value = 'Error';
    }
}
```
## poktmon
### html코드
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>pokemon</title>
    <link rel="stylesheet" href="./css/main.css">
    <script src="./js/main.js"></script>
</head>
<body>
    <div class="contain">
        <div class="cloud"><img src="./images/cloud_1.png" alt="구름_1"></div>
        <div class="cloud"><img src="./images/cloud_2.png" alt="구름_2"></div>
        <div class="cloud"><img src="./images/cloud_3.png" alt="구름_3"></div>
        <div class="logo">
            <img src="./images/logo.png" alt="포켓몬 로고">
        </div>
        <div class="inner">
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
           <div class="pokemon">
            <div class="images"></div>
           </div>
        </div>
    </div>
</body>
</html>
```
### css코드
```css
*{
    text-decoration: none;
}

body{
    background-image: url(../images/back.png);
    background-repeat: no-repeat;
    background-size: auto;
    overflow-x: hidden;
    height: 100vh;
   
}

/* 구름 넣기 */

.contain .cloud{
    position: absolute;
    z-index: -20;
}

.contain .cloud:nth-child(1){
    left: -300px;
    animation: 300s ease-in 1s infinite reverse both running cloud1;
}
@keyframes cloud1 {
    from {
      
      transform: translateX(250vh);
    }
    to {
     
      transform: translateX(0);
    }
  }

  .contain .cloud:nth-child(2){
    right: -700px;
    animation: 150s ease-in 1s infinite reverse both running cloud2;
}
@keyframes cloud2 {
    from {
     
      transform: translate(-250vh);
    }
    to {
     
      transform: translateX(0);
    }
  }

  .contain .cloud:nth-child(3){
    top: 500px;
    left: 100px;
    animation: 130s ease-in 1s infinite reverse both running cloud3;
}
@keyframes cloud3 {
    from {
     
      transform: translate(250vh);
    }
    to {
     
      transform: translateX(0);
    }
  }

  /* 기본 잡기 */
.contain .inner{
    max-width: 1100px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 auto;
    padding: 40px 20px;
}
/* 로고 넣기 */
.contain .logo{
   margin-top: 120px;


}
.contain .logo img{
    width: 450px;
    display: block;
    margin: 0 auto;
    
}
/* 포켓몬 볼 삽입 */
.contain .inner .pokemon{
    width: 150px;
    height: 150px;
    background-image: url(../images/ball.png);
    background-size: contain;
    margin: 30px;
    transition: transform .2s,;
}

.contain .inner .pokemon .images{
    width: 100%;
    height: 100%;
    background-position: center;
    background-size: 80px;
} 

/* 포켓몬 hover */
.contain .inner .pokemon:hover{
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    transform: scale(1.5);
    z-index: 1;
}

.contain .inner .pokemon:nth-child(1):hover{ background-image: url(../images/pokemon_1.png);}
.contain .inner .pokemon:nth-child(2):hover{ background-image: url(../images/pokemon_2.png);}
.contain .inner .pokemon:nth-child(3):hover{ background-image: url(../images/pokemon_3.png);}
.contain .inner .pokemon:nth-child(4):hover{ background-image: url(../images/pokemon_4.png);}
.contain .inner .pokemon:nth-child(5):hover{ background-image: url(../images/pokemon_5.png);}
.contain .inner .pokemon:nth-child(6):hover{ background-image: url(../images/pokemon_6.png);}
.contain .inner .pokemon:nth-child(7):hover{ background-image: url(../images/pokemon_7.png);}
.contain .inner .pokemon:nth-child(8):hover{ background-image: url(../images/pokemon_8.png);}
.contain .inner .pokemon:nth-child(9):hover{ background-image: url(../images/pokemon_9.png);}
.contain .inner .pokemon:nth-child(10):hover{ background-image: url(../images/pokemon_10.png);}
.contain .inner .pokemon:nth-child(11):hover{ background-image: url(../images/pokemon_11.png);}
.contain .inner .pokemon:nth-child(12):hover{ background-image: url(../images/pokemon_12.png);}
.contain .inner .pokemon:nth-child(13):hover{ background-image: url(../images/pokemon_13.png);}
.contain .inner .pokemon:nth-child(14):hover{ background-image: url(../images/pokemon_14.png);}
.contain .inner .pokemon:nth-child(15):hover{ background-image: url(../images/pokemon_15.png);}

```

