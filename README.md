# birthday
Surprise plan
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Kuku 💗</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Trebuchet MS", sans-serif;
  background: linear-gradient(135deg, #ffe4ef, #fff5fa, #eadfff);
  color: #873b66;
  text-align: center;
  overflow-x: hidden;
}

.hero {
  min-height: 100vh;
  padding: 45px 18px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.card {
  max-width: 500px;
  width: 100%;
  padding: 28px 20px;
  background: rgba(255,255,255,0.85);
  border: 2px solid white;
  border-radius: 30px;
  box-shadow: 0 12px 40px #c85c9430;
  backdrop-filter: blur(5px);
}

.tag {
  display: inline-block;
  padding: 8px 15px;
  background: #ffe0ec;
  border-radius: 25px;
  font-size: 13px;
  font-weight: bold;
}

h1 {
  font-size: clamp(34px, 9vw, 50px);
  line-height: 1.15;
  color: #ed5796;
  margin: 20px 0 8px;
}

h2 {
  color: #d44f89;
  margin-top: 10px;
}

p {
  line-height: 1.8;
}

.bear {
  font-size: 82px;
  animation: cuddle 2s infinite ease-in-out;
  cursor: pointer;
  display: inline-block;
}

button {
  padding: 14px 23px;
  border: 0;
  border-radius: 30px;
  color: white;
  background: linear-gradient(90deg, #ff629b, #c77dff);
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 5px 18px #dc6ca64c;
  margin: 10px 4px;
  transition: transform 0.2s;
}

button:active {
  transform: scale(0.95);
}

.section {
  max-width: 650px;
  width: 92%;
  margin: 30px auto;
  padding: 28px 20px;
  background: #fffafd;
  border: 2px dashed #f5a7cb;
  border-radius: 25px;
  box-shadow: 0 8px 25px #c85c9415;
}

/* Interactive Candle & Cake Styles */
.cake-container {
  position: relative;
  display: inline-block;
  margin: 20px 0;
  cursor: pointer;
}

.candle-flame {
  font-size: 30px;
  position: absolute;
  top: -25px;
  left: 50%;
  transform: translateX(-50%);
  animation: flicker 0.8s infinite alternate;
  transition: opacity 0.5s ease;
}

.cake-emoji {
  font-size: 85px;
  transition: transform 0.5s ease;
}

.cut-effect {
  animation: slice 0.6s ease forwards;
}

/* Interactive Gift Grid */
.gifts-grid {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin: 20px 0;
}

.gift-box {
  background: #ffe3f0;
  border: 2px solid #ff92c2;
  border-radius: 20px;
  padding: 20px;
  width: 130px;
  cursor: pointer;
  font-size: 40px;
  transition: transform 0.3s, background 0.3s;
}

.gift-box:hover {
  transform: translateY(-5px);
}

.gift-box.opened {
  background: #ffffff;
  border-color: #c77dff;
}

.gift-text {
  font-size: 13px;
  color: #873b66;
  margin-top: 10px;
  font-weight: bold;
  display: none;
}

/* Hug Box Animation */
.hug-box {
  font-size: 90px;
  margin: 15px 0;
  transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.hug-active {
  transform: scale(1.3) rotate(5deg);
}

/* Floating Animation */
.floating {
  position: fixed;
  top: -40px;
  pointer-events: none;
  z-index: 999;
  animation: fall linear forwards;
}

@keyframes cuddle {
  0%, 100% { transform: rotate(-5deg) translateY(0); }
  50% { transform: rotate(5deg) translateY(-9px); }
}

@keyframes flicker {
  0% { transform: translateX(-50%) scale(1); opacity: 1; }
  100% { transform: translateX(-50%) scale(1.2); opacity: 0.8; }
}

@keyframes slice {
  0% { transform: scale(1); }
  50% { transform: scale(1.1) rotate(5deg); }
  100% { transform: scale(1) rotate(0deg); }
}

@keyframes fall {
  to { transform: translateY(115vh) rotate(360deg); }
}

footer {
  padding: 30px 15px 45px;
  color: #b83e7b;
}
</style>
</head>

<body>

<!-- STEP 1: HERO SURPRISE -->
<section class="hero">
  <div class="card">
    <div class="tag">🎀 A little surprise made with love 🎀</div>

    <div class="bear" onclick="celebrate()">🧸💗</div>

    <p>To my favorite girl in the whole world</p>

    <h1>Happy Birthday,<br>Kuku! 🎂</h1>

    <p>
      Today is all about you, my princess.
      You deserve a thousand smiles and a million hugs. 💕
    </p>

    <button onclick="scrollToSection('cake-section')">
      Open Your Surprise 💌
    </button>

    <p style="font-size:12px; opacity:0.8;">Made specially for you by your Jaan ❤️</p>
  </div>
</section>

<!-- STEP 2 & 3: CANDLE BLOW & CAKE CUT -->
<section class="section" id="cake-section">
  <h2>Make a Birthday Wish! ✨</h2>
  <p>Tap the flame to blow out the candle! 🕯️</p>

  <div class="cake-container" onclick="blowCandle()">
    <div class="candle-flame" id="flame">🔥</div>
    <div class="cake-emoji" id="cakeEmoji">🎂</div>
  </div>

  <div id="candleText" style="font-weight:bold; color:#ed5796;">Candle is glowing... Make a wish!</div>

  <br>
  <button id="cutCakeBtn" onclick="cutCake()" style="display:none;">
    Cut The Birthday Cake 🔪🎂
  </button>
</section>

<!-- STEP 4: VIRTUAL GIFTS -->
<section class="section" id="gifts-section" style="display:none;">
  <h2>Unwrap Your Birthday Gifts 🎁</h2>
  <p>Tap each present box to see what's inside!</p>

  <div class="gifts-grid">
    <div class="gift-box" onclick="openGift(this, '👑 Unlimited Hugs & Kisses')">
      🎁
      <div class="gift-text"></div>
    </div>
    <div class="gift-box" onclick="openGift(this, '🌷 A Lifetime of Happiness')">
      🎁
      <div class="gift-text"></div>
    </div>
    <div class="gift-box" onclick="openGift(this, '💖 Endless Love & Care')">
      🎁
      <div class="gift-text"></div>
    </div>
  </div>

  <button onclick="scrollToSection('letter-section')">Read Your Card 💌</button>
</section>

<!-- STEP 5: BIRTHDAY CARD & LETTER -->
<section class="section" id="letter-section" style="display:none;">
  <div style="font-size:55px">💌</div>
  <h2>A Letter For My Kuku</h2>

  <p style="text-align:left">
    Hey, my Kuku! 🥹💗
    <br><br>
    Happy Birthday, meri jaan! 🎂❤️
    <br><br>
    I wish I could be beside you right now,
    holding your hand and watching you smile.
    You are someone very special to me, and I
    hope today gives you as much happiness as
    you bring into my life.
    <br><br>
    I love your smile, your little ways, and all
    the moments that make you YOU. You don't
    have to be perfect to be precious to me.
    Just keep being my lovely Kuku. 🧸
    <br><br>
    May Allah bless you with happiness, good
    health, success, peace, and everything
    beautiful your heart wishes for. Ameen. 🤲🏻
    <br><br>
    No matter how busy life gets, I hope you
    always remember how special you are.
    Today, tomorrow, and every birthday ahead,
    you deserve to feel loved.
    <br><br>
    <strong>Happy Birthday, meri Kuku! 🎀💋</strong>
    <br><br>
    Forever your Jaan,<br>
    <strong>Zain ❤️</strong>
  </p>

  <button onclick="scrollToSection('hug-section')">Next Surprise 🫂</button>
</section>

<!-- STEP 6: VIRTUAL HUG -->
<section class="section" id="hug-section" style="display:none;">
  <h2>Sending You A Big Warm Hug! 🫂</h2>
  <p>Tap the button below to get your warm bear hug!</p>

  <div class="hug-box" id="hugBox">🐻💖🐰</div>

  <button onclick="giveHug()">Give Kuku A Big Hug 💗</button>
</section>

<footer>
  Made with all my love 💗<br>
  <strong>Zain, her Jaan</strong><br>
  <span>Happy Birthday, Kuku! 🎂</span>
</footer>

<script>
function scrollToSection(id) {
  const el = document.getElementById(id);
  el.style.display = "block";
  el.scrollIntoView({ behavior: "smooth" });
  celebrate();
}

function blowCandle() {
  const flame = document.getElementById("flame");
  const candleText = document.getElementById("candleText");
  const cutBtn = document.getElementById("cutCakeBtn");

  flame.style.opacity = "0";
  candleText.innerText = "Yay! Your wish is sent to the stars! ✨";
  cutBtn.style.display = "inline-block";
  celebrate();
}

function cutCake() {
  const cake = document.getElementById("cakeEmoji");
  const candleText = document.getElementById("candleText");

  cake.classList.add("cut-effect");
  cake.innerText = "🍰🎂🍰";
  candleText.innerText = "Yummy cake sliced for Kuku! 😋";

  setTimeout(() => {
    scrollToSection("gifts-section");
  }, 1200);
}

function openGift(element, text) {
  element.classList.add("opened");
  element.querySelector(".gift-text").innerText = text;
  element.querySelector(".gift-text").style.display = "block";
  celebrate();
}

function giveHug() {
  const hugBox = document.getElementById("hugBox");
  hugBox.classList.add("hug-active");

  celebrate();

  setTimeout(() => {
    hugBox.classList.remove("hug-active");
  }, 1000);
}

function celebrate() {
  const symbols = ["💗", "💖", "💕", "🌸", "🎀", "✨", "❤️", "🎂", "🎈"];

  for (let i = 0; i < 40; i++) {
    setTimeout(() => {
      const item = document.createElement("div");
      item.className = "floating";
      item.textContent = symbols[Math.floor(Math.random() * symbols.length)];
      item.style.left = Math.random() * 100 + "vw";
      item.style.fontSize = (18 + Math.random() * 22) + "px";
      item.style.animationDuration = (3 + Math.random() * 3) + "s";

      document.body.appendChild(item);
      setTimeout(() => item.remove(), 6000);
    }, i * 40);
  }
}
</script>

</body>
</html>
