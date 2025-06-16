<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Trang Chủ Free Fire</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: url('https://i.imgur.com/dN1ZyzH.jpg') no-repeat center center/cover;
      color: #fff;
    }
    .container {
      text-align: center;
      background-color: rgba(0, 0, 0, 0.6);
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 0 20px #00ffcc;
    }
    h1 {
      font-size: 36px;
      margin-bottom: 20px;
    }
    p {
      font-size: 18px;
      margin-bottom: 30px;
    }
    .btn {
      background: #00ffcc;
      color: #000;
      border: none;
      padding: 15px 30px;
      font-size: 20px;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
      text-decoration: none;
    }
    .btn:hover {
      background: #00e6b8;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Chào mừng đến với sự kiện Free Fire</h1>
  <p>Nhận phần thưởng miễn phí mỗi ngày bằng cách quay vòng quay may mắn!</p>
  <a href="wheel.html" class="btn">🎯 Hãy nhập số điện thoại và faceobook của bạn vào đây</a>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Đăng Nhập Free Fire</title>
  <style>
    body {
      background: linear-gradient(to right, #1f4037, #99f2c8);
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .login-box {
      background: #ffffff;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
      text-align: center;
      width: 300px;
    }
    .login-box h2 {
      margin-bottom: 30px;
      color: #333;
    }
    .login-box input[type="text"],
    .login-box input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .login-box button {
      width: 100%;
      padding: 12px;
      background: #00cc99;
      border: none;
      color: #fff;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .login-box button:hover {
      background: #009973;
    }
    .error {
      color: red;
      font-size: 14px;
      display: none;
      margin-top: 10px;
    }
  </style>
</head>
<body>

<div class="login-box">
  <h2>Đăng Nhập</h2>
  <input type="text" id="username" placeholder="Tài khoản">
  <input type="password" id="password" placeholder="Mật khẩu">
  <button onclick="login()">Đăng nhập</button>
  <div id="error" class="error">Tài khoản hoặc mật khẩu không đúng</div>
</div>

<script>
  function login() {
    const user = document.getElementById('username').value;
    const pass = document.getElementById('password').value;
    const errorDiv = document.getElementById('error');

    // Đây chỉ là kiểm tra tạm thời (demo). Vui lòng nhập mật khẩu và tài khoản Facebook để vào vòng quay.
    if (user === '         ' && pass === '       ') {
      // Đăng nhập thành công, chuyển đến vòng quay
      window.location.href = 'wheel.html';
    } else {
      // Sai tài khoản hoặc sai mật khẩu
      errorDiv.style.display = 'block';
    }
  }
  <!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Vòng Quay Free Fire</title>
  <style>
    body {
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #1e1e1e;
      color: #fff;
    }
    .container {
      position: relative;
    }
    .wheel {
      width: 300px;
      height: 300px;
      border-radius: 50%;
      border: 10px solid #fff;
      position: relative;
      overflow: hidden;
      box-shadow: 0 0 20px #00ffcc;
      transform: rotate(0deg);
      transition: transform 5s cubic-bezier(0.33, 1, 0.68, 1);
    }
    .wheel .segment {
      position: absolute;
      width: 50%;
      height: 50%;
      top: 50%;
      left: 50%;
      transform-origin: 0% 0%;
      background: #ffcc00;
      text-align: right;
      padding-right: 10px;
      line-height: 3em;
      font-weight: bold;
    }
    .pointer {
      width: 0; 
      height: 0; 
      border-left: 20px solid transparent;
      border-right: 20px solid transparent;
      border-bottom: 30px solid red;
      position: absolute;
      top: -30px;
      left: 50%;
      transform: translateX(-50%);
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 18px;
      cursor: pointer;
      background: #00ffcc;
      border: none;
      border-radius: 5px;
      color: #000;
    }
  </style>
</head>
<body>

<div class="container">
  <div class="pointer"></div>
  <div class="wheel" id="wheel">
    <!-- 8 phần thưởng -->
    <div class="segment" style="transform: rotate(0deg); background: #ff6666;">1000 Kim Cương</div>
    <div class="segment" style="transform: rotate(45deg); background: #66ff66;">Skin Súng MP40 Mãng Xà và 200 Hộp nâng cấp súng</div>
    <div class="segment" style="transform: rotate(90deg); background: #6666ff;">Thẻ Boyaa </div>
    <div class="segment" style="transform: rotate(135deg); background: #ffff66;">Pet Shiba</div>
    <div class="segment" style="transform: rotate(180deg); background: #ff66ff;">500 Kim Cương</div>
    <div class="segment" style="transform: rotate(225deg); background: #66ffff;">Nấm đấm nhất quyền</div>
    <div class="segment" style="transform: rotate(270deg); background: #ff9966;">Ump KHủng long nhong nhong</div>
    <div class="segment" style="transform: rotate(315deg); background: #9999ff;">Áo cổ rùa </div>
  </div>
  <button onclick="spin()">Quay Ngay</button>
</div>

<script>
  function spin() {
    const wheel = document.getElementById("wheel");
    const rand = Math.floor(3600 + Math.random() * 360); // quay ít nhất 10 vòng
    wheel.style.transition = "transform 5s cubic-bezier(0.33, 1, 0.68, 1)";
    wheel.style.transform = `rotate(${rand}deg)`;
  }
</script>

</body>
</html>
const playerID = localStorage.getItem('playerID');
document.getElementById('welcomeText').textContent = 'Xin chào ID: ' + playerID;
