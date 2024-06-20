# IT-VISION-SCHOOL-CLASS
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

### 포트폴리오 css코드
```css
@import url('https://fonts.googleapis.com/css2?family=Alfa+Slab+One&family=Archivo+Black&display=swap');
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
@media (max-width: 768px){
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
    /* color: #0bf7ff; */
}

.menu-toggle{
    display: none;
    font-size: 30px;
    cursor: pointer;
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
    color: #0bf7ff;
    cursor: pointer;
}

@media (max-width:768px){
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
```
