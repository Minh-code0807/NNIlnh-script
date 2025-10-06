<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kiểm tra mã truy cập</title>
  <style>
    body {
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }
    .container {
      background: rgba(255, 255, 255, 0.9);
      padding: 35px 50px;
      border-radius: 20px;
      box-shadow: 0 0 25px rgba(0, 0, 0, 0.3);
      text-align: center;
      animation: fadeIn 0.8s ease;
    }
    h2 { color: #2a5298; margin-bottom: 20px; }
    input {
      width: 260px; padding: 10px; font-size: 16px;
      border: 2px solid #007BFF; border-radius: 8px;
      outline: none; text-align: center;
    }
    button {
      margin-top: 15px; padding: 10px 30px; font-size: 16px;
      background-color: #007BFF; color: white;
      border: none; border-radius: 8px;
      cursor: pointer; transition: 0.3s;
    }
    button:hover { background-color: #0056b3; transform: scale(1.05); }
    .message { margin-top: 15px; font-weight: bold; }
    @keyframes fadeIn { from { opacity: 0; transform: scale(0.9); } to { opacity: 1; transform: scale(1); } }
  </style>
</head>
<body>
  <div class="container">
    <h2>🔒 Nhập mã truy cập</h2>
    <input type="text" id="inputCode" placeholder="Nhập mã tại đây...">
    <br>
    <button onclick="checkCode()">Xác nhận</button>
    <div class="message" id="message"></div>
  </div>

  <script>
    function checkCode() {
      const userInput = document.getElementById("inputCode").value.trim();
      const message = document.getElementById("message");
      const code1 = "mmhg3k";
      const code2 = "quangdai173";

      if (userInput === code1) {
        message.style.color = "green";
        message.textContent = "✅ Mã đúng! Đang chuyển hướng...";
        setTimeout(() => {
          window.top.location.href = "https://sites.google.com/view/thinhscripts/trang-ch%E1%BB%A7";
        }, 800);
      } else if (userInput === code2) {
        message.style.color = "green";
        message.textContent = "✅ Mã đúng! Đang chuyển hướng...";
        setTimeout(() => {
          window.top.location.href = "https://sites.google.com/view/getsolarabootstrapper/trang-ch%E1%BB%A7";
        }, 800);
      } else {
        message.style.color = "red";
        message.textContent = "❌ Sai mã! Thử lại nhé.";
      }
    }
  </script>
</body>
</html>
