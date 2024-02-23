
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Moving Circle</title>
  <style>
    #canvas {
      border: 1px solid black;
    }
  </style>
</head>
<body>
  <canvas id="canvas" width="600" height="400"></canvas>

  <script>
    // Get the canvas element and its context
    var canvas = document.getElementById('canvas');
    var ctx = canvas.getContext('2d');

    // Set initial position and velocity
    var x = canvas.width / 2;
    var y = canvas.height / 2;
    var dx = 2;
    var dy = -2;
    var radius = 20;

    function drawCircle() {
      // Clear the canvas
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw the circle
      ctx.beginPath();
      ctx.arc(x, y, radius, 0, Math.PI * 2);
      ctx.fillStyle = 'blue';
      ctx.fill();
      ctx.closePath();

      // Update the circle's position
      x += dx;
      y += dy;

      // Reverse direction if circle reaches canvas boundary
      if (x + dx > canvas.width - radius || x + dx < radius) {
        dx = -dx;
      }
      if (y + dy > canvas.height - radius || y + dy < radius) {
        dy = -dy;
      }
    }

    // Update the animation frame
    function update() {
      drawCircle();
      requestAnimationFrame(update);
    }

    // Start the animation
    update();
  </script>
</body>
</html>


</head>
<body>
  <button id="startButton">Start</button>
  <button id="stopButton" disabled>Stop</button>

  








<!---
DAVgghvg/DAVgghvg is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
