# lovebyme
heartwithher
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Heart Shape</title>
<style>
  .heart {
    width: 100px;
    height: 100px;
    background-color: red;
    position: relative;
    margin: auto;
    transform: rotate(-45deg);
  }

  .heart:before,
  .heart:after {
    content: '';
    width: 100px;
    height: 100px;
    border-radius: 50px;
    background-color: red;
    position: absolute;
  }

  .heart:before {
    top: 0;
    left: 50px;
  }

  .heart:after {
    top: -50px;
    left: 0;
  }

  .heart-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 24px;
    color: white;
    font-weight: bold;
  }
</style>
</head>
<body>
  <a href="#" onclick="showHeart('Farah');">Click me</a>
  <div class="heart" id="heart" style="display: none;">
    <div class="heart-text" id="heartText"></div>
  </div>
  <script>
    function showHeart(name) {
      const heart = document.getElementById('heart');
      const heartText = document.getElementById('heartText');
      heart.style.display = 'block';
      heartText.innerText = name;
    }
  </script>
</body>
</html>
