<script>
const API_URL = "https://moaeen-triage-backend-production.up.railway.app/api/chat";

const form = document.getElementById("chat-form");
const input = document.getElementById("user-input");
const chatBox = document.getElementById("chat-box");

form.addEventListener("submit", async (e) => {
  e.preventDefault();

  const userText = input.value.trim();
  if (!userText) return;

  chatBox.innerHTML += `<div><b>👤 You:</b> ${userText}</div>`;
  input.value = "";

  chatBox.innerHTML += `<div id="typing">🤖 AI is typing...</div>`;

  try {
    const res = await fetch(API_URL, {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ message: userText })
    });

    const data = await res.json();
    document.getElementById("typing").remove();

    chatBox.innerHTML += `<div><b>🤖 Moaeen AI:</b> ${data.reply}</div>`;
  } catch {
    document.getElementById("typing").remove();
    chatBox.innerHTML += `<div style="color:red">❌ AI Error</div>`;
  }
});
</script>
