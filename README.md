<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>HBD🌻</title>
<style>
  body {
    margin: 0;
    font-family: "Comic Sans MS", cursive;
    background-color: #fff3b0; /* soft butter yellow */
    overflow-x: hidden;
    color: #5a3e00;
    text-align: center;
  }

  h1 {
    font-size: 3em;
    color: #e1a100;
    margin-top: 50px;
    text-shadow: 2px 2px #fff5c3;
  }

  p {
    font-size: 1.3em;
    margin: 15px auto;
    max-width: 600px;
    line-height: 1.6em;
  }

  .btn {
    display: inline-block;
    background-color: #ffd54f;
    color: #5a3e00;
    padding: 12px 30px;
    margin: 15px;
    border-radius: 30px;
    font-size: 1.2em;
    border: none;
    cursor: pointer;
    transition: 0.3s;
    box-shadow: 0 4px 8px rgba(255, 204, 0, 0.3);
  }

  .btn:hover {
    background-color: #ffecb3;
    transform: scale(1.1);
  }

  .msg-box {
    margin-top: 30px;
    font-size: 1.2em;
    background: #fff9c4;
    display: inline-block;
    padding: 20px 25px;
    border-radius: 20px;
    box-shadow: 0 0 10px rgba(255, 204, 0, 0.3);
  }

  /* Floating balloons with ribbons */
  .balloons span {
    position: fixed;
    bottom: -100px;
    width: 40px;
    height: 60px;
    border-radius: 50%;
    background-color: #f48fb1;
    animation: rise 7s linear infinite;
    opacity: 0.9;
  }

  /* Add ribbon/string using pseudo-element */
  .balloons span::after {
    content: "";
    position: absolute;
    left: 50%;
    bottom: -40px;
    width: 2px;
    height: 45px;
    background: linear-gradient(to bottom, #d4af37, #ffeb3b);
    transform: translateX(-50%);
    border-radius: 2px;
  }

  /* Different colors and delays */
  .balloons span:nth-child(1) { left: 10%; background-color: #f48fb1; animation-delay: 0s; }
  .balloons span:nth-child(2) { left: 25%; background-color: #ffcc80; animation-delay: 2s; }
  .balloons span:nth-child(3) { left: 45%; background-color: #81d4fa; animation-delay: 4s; }
  .balloons span:nth-child(4) { left: 65%; background-color: #a5d6a7; animation-delay: 1s; }
  .balloons span:nth-child(5) { left: 80%; background-color: #ce93d8; animation-delay: 3s; }

  @keyframes rise {
    0% { transform: translateY(0) scale(1); opacity: 1; }
    100% { transform: translateY(-110vh) scale(1.2); opacity: 0; }
  }
</style>
</head>
<body>

<div class="balloons">
  <span></span><span></span><span></span><span></span><span></span>
</div>

<h1>🌻 Happy Birthday Rani-Pani Tai 🌻</h1>
<h2 style="color:#e1a100; font-weight:bold;">🎉 Celebrating Beautiful 25 Years 🎉</h2>

<p>Dear Tai, you are the sunshine that fills every heart with warmth 🌞💛  
<br>May your 25th year be as bright, gentle, and golden as your soul.  
<br>Keep smiling, keep shining you truly make life more beautiful! 🌸</p>

<div>
  <button class="btn" onclick="showWish()">Make a Wish💌</button>
  <button class="btn" onclick="playSong()">Let's sing a song🎵</button>
</div>

<div id="wishBox" class="msg-box" style="display:none;"></div>

<audio id="birthdaySong" src="birthday.mp3"></audio>

<script>
function showWish() {
  const msgs = [
    "May your day bloom like a sunflower in sunshine!🌼 ",
    "You deserve all the happiness and love today, always and forever!🌟 ",
    "Keep shining, TaiPai — you’re golden inside and out!💛 ",
    "Wishing you endless smiles and sunflower fields forever!🌸 ",
    "Forever my gossip buddy, my Scorpio twin happy 25th!💖 ",
    "You are stronger, wiser, and more capable than you’ll ever realize!💫",
    "Dear Rani-Pani Tai 💖 <br>Happy Silver Jubilee, my forever Scorpio partner!♏✨ <br>May your 25th year bring calm skies, warm hearts, and infinite joy. <br>You’re truly one in a million radiant, strong, and full of that magical Scorpio energy we both know so well.<br>Watching you bloom into such a beautiful, kind, and powerful soul fills me with endless pride.<br> You’ve come so far and have so much light ahead of you.<br> Here’s to new adventures, deeper laughter, and dreams that shine brighter than ever.<br> Love you loads, Tai 🌸<br> Can’t wait for more late-night talks, endless gossip, and more memories that we’ll cherish forever.💕"
  ];
  const msg = msgs[Math.floor(Math.random() * msgs.length)];
  const box = document.getElementById("wishBox");
  box.style.display = "inline-block";
  box.innerHTML = msg;
}

function playSong() {
  const song = document.getElementById("birthdaySong");
  song.play();
  alert("Let's gooo — 1...2...3...🎂");
}
</script>

</body>
</html>
