# IT-VISION-SCHOOL-CLASS
## HTML, CSS를 활용한 움직이는 정육면체 만들기

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
