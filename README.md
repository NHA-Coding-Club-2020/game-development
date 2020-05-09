# NHA Coding Club 2020 - Build a Game in HTML, CSS, and JavaScript
We're going to build a game!

# Week 2 Assignment
Step 1. From the your.name branch open Gitpod

Step 2. Merge the code from assignments/week-2 branch

Step 3. Open "game.html"

Step 4. Update the ```<title></title>``` tag to match below - STOP AND SHOW!

```
<title>Move the Dot Game</title>
```


Step 5. Update the CSS code for ```.wrapper {}``` class to match below - STOP AND SHOW!

```
   .wrapper {
       height: 50%;
       border: 5px purple dotted;
       width: 600px;
       margin-top: 50px;
       margin-bottom: 50px;
       margin-left: auto;
       margin-right: auto;
       padding: 40px;
   }
```

Step 6. Update the ```<div>``` tags to be like below - STOP AND SHOW!

```
<div class="wrapper">
    <div style="font-size:20px; cursor: pointer;">
    Welcome to Move the Dot - A Game of Skill (Sort of)!!
    </div>

    <canvas class="game-board">Your browser does not support canvas.</canvas>
    
    <button class="start-game">Start Game</button>
    <button class="reset-game">Reset</button>
</div>
```

Step 7. Update your ```<script></script>``` tag to be the following - STOP AND SHOW!

```
<script>
    var canvas = $('canvas.game-board');
    var context = canvas[0].getContext('2d');
    var canvasWidth = canvas.width();
    var canvasHeight = canvas.height();
    canvas.attr({height: canvasHeight, width: canvasWidth});
    var frames = 150;
    var currentFrame = 0;
    var dot = { x: 50, y: 50, radius: 25 };
    drawDot(dot);

    function drawDot(dot) {
        context.beginPath();
        context.arc(dot.x, dot.y, dot.radius, 0, 2 * Math.PI, false);
        context.fillStyle = '#F03C69';
        context.fill();
    }
</script>

Step 8. Add the following to the bottom your script tag ```<script>``` tag - STOP AND SHOW!

```
    function moveDot() {
        context.clearRect(0, 0, canvasWidth, canvasHeight);
        dot.x += 1;
        dot.y += 1;
        drawDot(dot);
        currentFrame += 1;
        if( currentFrame == frames ) {
            currentFrame = 0;
            dot = { x: 50, y: 50, radius: 25 };
        }

        window.requestAnimationFrame(moveDot);
    }

    $(".start-game").on("click", function() {
        window.requestAnimationFrame(moveDot);
    });
```

