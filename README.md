<!DOCTYPE html>
<html>
<head>
  <title>Valentine 💖</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #ffd6e7;
      padding-top: 80px;
    }

    h1 {
      color: #ff4d94;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      margin: 10px;
      border-radius: 20px;
      border: none;
      cursor: pointer;
    }

    #yes {
      background-color: #ff66a3;
      color: white;
    }

    #no {
      background-color: #cccccc;
      position: absolute;
    }

    #cat, #gifts, .photo {
      display: none;
      margin-top: 20px;
    }

    .gift {
      font-size: 50px;
      cursor: pointer;
      margin: 20px;
    }

    img {
      width: 250px;
      border-radius: 15px;
      margin-top: 15px;
    }
  </style>
</head>

<body>

<h1>Would you like to be my valentine? 💌</h1>

<button id="yes" onclick="sayYes()">YES</button>
<button id="no" onclick="moveNo()">NO</button>

<div id="cat">
  <h2>YEYYY!! 🐱💖</h2>
  <img src="cat.jpg">
</div>

<div id="gifts">
  <div class="gift" onclick="showPhoto(1)">🎁</div>
  <div class="gift" onclick="showPhoto(2)">🎁</div>
  <div class="gift" onclick="showPhoto(3)">🎁</div>
</div>

<div id="photo1" class="photo">
  <img src="foto1.jpg">
</div>

<div id="photo2" class="photo">
  <img src="foto2.jpg">
</div>

<div id="photo3" class="photo">
  <img src="foto3.jpg">
</div>

<script>
function sayYes() {
  document.getElementById("cat").style.display = "block";
  document.getElementById("gifts").style.display = "block";
}

function moveNo() {
  var x = Math.random() * (window.innerWidth - 100);
  var y = Math.random() * (window.innerHeight - 50);
  var btn = document.getElementById("no");
  btn.style.left = x + "px";
  btn.style.top = y + "px";
}

function showPhoto(num) {
  document.getElementById("photo" + num).style.display = "block";
}
</script>

</body>
</html>
