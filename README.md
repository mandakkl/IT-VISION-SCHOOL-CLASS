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
## ${{color{#6580DD}디지털 시계 만들기}}$
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
```
