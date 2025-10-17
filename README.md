<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gửi cậu nhân ngày 20/10 💐</title>
<style>
  body {
    background: linear-gradient(180deg, #fde2f3, #fff0f6);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-family: "Segoe UI", sans-serif;
    text-align: center;
    margin: 0;
  }

  h2 {
    color: #d63384;
    margin-bottom: 20px;
  }

  .gift-box {
    width: 150px;
    height: 150px;
    background: #ff7eb9;
    border-radius: 10px;
    position: relative;
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    transition: transform 0.3s ease;
  }

  .gift-lid {
    width: 150px;
    height: 30px;
    background: #ff5fa2;
    border-radius: 8px 8px 0 0;
    position: absolute;
    top: -30px;
    left: 0;
    transform-origin: bottom center;
    transition: transform 0.5s ease;
  }

  .ribbon {
    width: 100%;
    height: 20px;
    background: #ffb6c1;
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-50%);
  }

  .ribbon::before {
    content: "";
    width: 20px;
    height: 100%;
    background: #ffb6c1;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
  }

  .message {
    margin-top: 40px;
    font-size: 18px;
    color: #333;
    opacity: 0;
    transition: opacity 1.5s ease;
  }

  .show {
    opacity: 1;
  }

  .open .gift-lid {
    transform: rotateX(150deg);
  }
</style>
</head>
<body>

<h2>🎀 Cậu ơi, tớ có món quà nhỏ tặng cậu 🎁</h2>
<div class="gift-box" onclick="openGift()">
  <div class="gift-lid"></div>
  <div class="ribbon"></div>
</div>

<p id="msg" class="message">
  🌸 Chúc cậu 20/10 thật vui vẻ và hạnh phúc nha 💐<br>
  Cậu luôn xinh đẹp, tự tin và được yêu thương thật nhiều 💖<br>
  Tớ mong mọi điều tốt đẹp nhất sẽ đến với cậu 🎀
</p>

<audio id="music" src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_4e3c2d4a2a.mp3?filename=sad-piano-soft-ambient-10744.mp3"></audio>

<script>
  function openGift() {
    const box = document.querySelector('.gift-box');
    const msg = document.getElementById('msg');
    const music = document.getElementById('music');
    box.classList.add('open');
    msg.classList.add('show');
    music.play();
  }
</script>

</body>
</html>
