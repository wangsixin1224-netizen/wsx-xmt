<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<title>王英俊老婆专属七夕刮刮卡🍾🍾🍾</title>
<style>
  body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: "Arial", sans-serif;
    background: url('https://i.ibb.co/7J443VcF/image.jpg') no-repeat center center fixed;
    background-size: cover;
    overflow: hidden;
  }
  h1 {
    text-align: center;
    color: #fff;
    text-shadow: 2px 2px 5px #000;
    margin-top: 20px;
  }
  .container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin-top: 30px;
  }
  .scratch-card {
    width: 120px;
    height: 120px;
    margin: 10px;
    position: relative;
    cursor: pointer;
    border-radius: 10px;
    overflow: hidden;
  }
  .scratch-card img {
    width: 100%;
    height: 100%;
    display: block;
  }
  canvas {
    position: absolute;
    top: 0;
    left: 0;
  }
  audio {
    display: none;
  }
</style>
</head>
<body>
<h1>王英俊老婆专属七夕刮刮卡🍾🍾🍾</h1>
<div class="container">
  <div class="scratch-card"><img src="https://i.ibb.co/mrsyHD3c/1.png" alt="礼物1"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/8DCcN5pr/2.jpg" alt="礼物2"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/b5B9pCY6/3.jpg" alt="礼物3"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/ZzzscCVM/4.jpg" alt="礼物4"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/GfCQm2rb/5.jpg" alt="礼物5"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/1JKRTrKC/6.jpg" alt="礼物6"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/ymqJfCr0/7.jpg" alt="礼物7"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/xS7RwzBq/8.jpg" alt="礼物8"></div>
  <div class="scratch-card"><img src="https://i.ibb.co/Df43fpcJ/9.jpg" alt="礼物9"></div>
</div>

<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
document.querySelectorAll('.scratch-card').forEach(card => {
  const canvas = document.createElement('canvas');
  canvas.width = card.offsetWidth;
  canvas.height = card.offsetHeight;
  card.appendChild(canvas);
  const ctx = canvas.getContext('2d');

  // 覆盖层
  ctx.fillStyle = '#C0C0C0';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  let isDrawing = false;
  canvas.addEventListener('mousedown', () => { isDrawing = true; });
  canvas.addEventListener('mouseup', () => { isDrawing = false; });
  canvas.addEventListener('mouseleave', () => { isDrawing = false; });

  canvas.addEventListener('mousemove', e => {
    if (!isDrawing) return;
    const rect = canvas.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    ctx.globalCompositeOperation = 'destination-out';
    ctx.beginPath();
    ctx.arc(x, y, 15, 0, Math.PI * 2);
    ctx.fill();
  });

  canvas.addEventListener('touchmove', e => {
    e.preventDefault();
    const rect = canvas.getBoundingClientRect();
    const touch = e.touches[0];
    const x = touch.clientX - rect.left;
    const y = touch.clientY - rect.top;
    ctx.globalCompositeOperation = 'destination-out';
    ctx.beginPath();
    ctx.arc(x, y, 15, 0, Math.PI * 2);
    ctx.fill();
  }, { passive: false });
});
</script>
</body>
</html>
# wsx-xmt
