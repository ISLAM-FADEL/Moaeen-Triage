<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>Moaeen AI Chat</title>
  <style>
    body {
      font-family: Arial;
      background: #f5f5f5;
      padding: 20px;
    }
    #chat-box {
      background: white;
      padding: 15px;
      height: 400px;
      overflow-y: auto;
      border-radius: 8px;
      margin-bottom: 10px;
    }
    input {
      width: 80%;
      padding: 10px;
    }
    button {
      padding: 10px 15px;
    }
  </style>
</head>

<body>

<h2>🤖 Moaeen AI</h2>

<div id="chat-box"></div>

<form id="chat-form">
  <input id="user-input" placeholder="اكتب سؤالك هنا..." />
  <button type="submit">إرسال</button>
</form>

<script>
const API_URL = "https://moaeen-triage-backend-production.up.railway.app/api/chat";

const form = document.getElementById("chat-form");
const input = document.getElementById("user-input");
const chatBox = document.getElementById("chat-box");

form.addEventListener("submit", async (e) => {
  e.preventDefault();

  const text = input.value.trim();
  if (!text) return;

  chatBox.innerHTML += `<div><b>👤 أنت:</b> ${text}</div>`;
  input.value = "";

  const typing = document.createElement("div");
  typing.innerHTML = "🤖 جاري التفكير...";
  typing.id = "typing";
  chatBox.appendChild(typing);

  try {
    const res = await fetch(API_URL, {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ message: text })
    });

    const data = await res.json();
    document.getElementById("typing").remove();

    chatBox.innerHTML += `<div><b>🤖 معين:</b> ${data.reply}</div>`;
    chatBox.scrollTop = chatBox.scrollHeight;

  } catch (err) {
    document.getElementById("typing").remove();
    chatBox.innerHTML += `<div style="color:red">❌ حصل خطأ</div>`;
  }
});
</script>

</body>
</html>
