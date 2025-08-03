<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8" />
  <title>Тест Summer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #cde7f0; /* ніжно-блакитний */
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #003344;
    }
    #test-wrapper {
      background: #e6f2f8; /* світло-блакитний */
      border-radius: 15px;
      padding: 30px 40px;
      width: 700px;
      box-shadow: 0 0 20px rgba(0,51,68,0.3);
      color: #003344;
      position: relative;
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    h1 {
      font-size: 2.5em;
      color: #0077aa;
      margin-top: 0;
      margin-bottom: 20px;
    }
    input, button {
      font-size: 1.2em;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1.5px solid #0077aa;
      color: #003344;
      text-align: center;
    }
    input[type="text"] {
      width: 350px;
      text-align: center;
    }
    button {
      cursor: pointer;
      background-color: #0077aa;
      color: #e6f2f8;
      font-weight: bold;
      transition: background-color 0.3s ease;
      border: none;
      min-width: 100px;
    }
    button:hover:not(:disabled) {
      background-color: #005f7a;
    }
    button:disabled {
      background-color: #99bcd8;
      cursor: default;
      color: #666;
    }
    #result {
      margin-top: 30px;
      text-align: left;
      max-width: 650px;
      background: #d0e6f2;
      padding: 20px;
      border: 2px solid #0077aa;
      border-radius: 10px;
      box-shadow: 0 0 15px #0077aa33;
      color: #003344;
      align-self: center;
    }
    #timer {
      font-size: 1.5em;
      margin-bottom: 15px;
      color: #004466;
      text-align: center;
      width: 100%;
    }
    #test-container {
      display: none;
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    #start-container {
      margin-top: 0;
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    #user-name-display {
      font-size: 1.3em;
      margin-bottom: 15px;
      color: #0077aa;
      text-align: center;
    }
    #question-container {
      width: 100%;
      max-width: 600px;
      margin-bottom: 15px;
    }
    #question-number, #uk-word {
      margin: 10px 0;
    }
    #question-number {
      font-weight: bold;
    }
    #answer {
      width: 100%;
      box-sizing: border-box;
    }
    #buttons-nav {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }
    #finishBtn {
      min-width: 120px;
    }
    #exitBtn {
      position: absolute;
      top: 15px;
      right: 15px;
      background-color: #cc0000;
      color: #fff;
      border: none;
      font-weight: bold;
      cursor: pointer;
      padding: 8px 14px;
      border-radius: 6px;
      transition: background-color 0.3s ease;
      min-width: auto;
      width: auto;
    }
    #exitBtn:hover {
      background-color: #990000;
    }
  </style>
</head>
<body>

<div id="test-wrapper">
  <h1>Тест Summer</h1>

  <button id="exitBtn" onclick="location.reload()" title="Вихід">Вихід</button>

  <div id="start-container">
    <input type="text" id="userName" placeholder="Введіть Прізвище Ім'я По батькові" />
    <button id="startBtn">Почати тест</button>
  </div>

  <div id="test-container">
    <div id="user-name-display"></div>
    <div id="timer">Час: 10:00</div>

    <div id="question-container">
      <h2 id="question-number"></h2>
      <h3 id="uk-word"></h3>
      <input type="text" id="answer" placeholder="Введіть англійське слово" autocomplete="off" />
      <div><button id="confirmBtn">Підтвердити відповідь</button></div>
    </div>

    <div id="buttons-nav">
      <button id="prevBtn">Назад</button>
      <button id="nextBtn">Вперед</button>
      <button id="finishBtn" style="display:none;">Результат</button>
    </div>

    <div id="result" style="display:none;"></div>
  </div>
</div>

<script>
let words = [
  {uk:"Астронавт", en:"astronaut"}, {uk:"Планета", en:"planet"}, {uk:"Зірка", en:"star"},
  {uk:"Місяць", en:"moon"}, {uk:"Галактика", en:"galaxy"}, {uk:"Космос", en:"space"},
  {uk:"Прибулець", en:"alien"}, {uk:"Пірат", en:"pirate"}, {uk:"Корабель", en:"ship"},
  {uk:"Скарб", en:"treasure"}, {uk:"Острів", en:"island"}, {uk:"Карта", en:"map"},
  {uk:"Компас", en:"compass"}, {uk:"Золото", en:"gold"}, {uk:"Савана", en:"savanna"},
  {uk:"Антарктида", en:"antarctica"}, {uk:"Пустеля", en:"desert"}, {uk:"Джунглі", en:"jungle"},
  {uk:"Океан", en:"ocean"}, {uk:"Закляття", en:"spell"}, {uk:"Зілля", en:"potion"},
  {uk:"Чарівник", en:"wizard"}, {uk:"Мітла", en:"broom"}, {uk:"Солодкий", en:"sweet"}
];

function shuffle(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
}

shuffle(words);

let current = 0;
let userAnswers = Array(words.length).fill("");
let locked = Array(words.length).fill(false);

const qNum = document.getElementById("question-number");
const ukWord = document.getElementById("uk-word");
const answer = document.getElementById("answer");
const prevBtn = document.getElementById("prevBtn");
const nextBtn = document.getElementById("nextBtn");
const finishBtn = document.getElementById("finishBtn");
const confirmBtn = document.getElementById("confirmBtn");
const resultBox = document.getElementById("result");
const timerEl = document.getElementById("timer");

const startContainer = document.getElementById("start-container");
const testContainer = document.getElementById("test-container");
const userNameInput = document.getElementById("userName");
const userNameDisplay = document.getElementById("user-name-display");

let timerInterval;
let timeLeft = 600; // 10 хв

function updateUI() {
  qNum.textContent = `Питання ${current + 1} із ${words.length}`;
  ukWord.textContent = words[current].uk;
  answer.value = userAnswers[current];
  answer.disabled = locked[current];
  confirmBtn.disabled = locked[current];
  prevBtn.disabled = current === 0;
  nextBtn.style.display = current === words.length - 1 ? "none" : "inline-block";
  finishBtn.style.display = current === words.length - 1 ? "inline-block" : "none";
}

confirmBtn.addEventListener("click", () => {
  if (!locked[current]) {
    userAnswers[current] = answer.value.trim();
    locked[current] = true;
    answer.disabled = true;
    confirmBtn.disabled = true;
  }
});

prevBtn.addEventListener("click", () => {
  if (current > 0) {
    current--;
    updateUI();
  }
});

nextBtn.addEventListener("click", () => {
  if (current < words.length - 1) {
    current++;
    updateUI();
  }
});

finishBtn.addEventListener("click", showResult);

function showResult() {
  clearInterval(timerInterval);
  let correct = 0;
  let html = `<h2>Результат тесту для ${userNameDisplay.textContent}</h2><ul>`;
  for (let i = 0; i < words.length; i++) {
    const ua = words[i].uk;
    const en = words[i].en;
    const user = userAnswers[i].toLowerCase();
    const isCorrect = user === en.toLowerCase();
    if (isCorrect) correct++;
    html += `<li>${ua} — ваша відповідь: <b>${userAnswers[i] || '(не відповіли)'}</b> — ${isCorrect ? "✅ правильно" : "❌ неправильно"} (правильно: ${en})</li>`;
  }
  const score = correct * 0.5;
  html += `</ul><h3>Ваш результат: ${score} з 12 балів</h3>`;
  resultBox.innerHTML = html;
  resultBox.style.display = "block";
  answer.disabled = true;
  confirmBtn.disabled = true;
  nextBtn.disabled = true;
  prevBtn.disabled = true;
  finishBtn.disabled = true;
}

// Таймер
function updateTimer() {
  const min = Math.floor(timeLeft / 60);
  const sec = timeLeft % 60;
  timerEl.textContent = `Час: ${min}:${sec < 10 ? "0" : ""}${sec}`;
  if (timeLeft <= 0) {
    showResult();
  }
  timeLeft--;
}

document.getElementById("startBtn").addEventListener("click", () => {
  const name = userNameInput.value.trim();
  if (name === "") {
    alert("Будь ласка, введіть Прізвище Ім'я По батькові");
    return;
  }
  userNameDisplay.textContent = name;
  startContainer.style.display = "none";
  testContainer.style.display = "flex";
  updateUI();
  timerInterval = setInterval(updateTimer, 1000);
});
</script>

</body>
</html>
