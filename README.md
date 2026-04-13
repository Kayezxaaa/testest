<<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You</title>

<style>
* {
  box-sizing: border-box;
  font-family: "Georgia", serif;
}

body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ffd6e8, #ffc3a0);
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

/* HIDDEN TOGGLE */
#open {
  display: none;
}

/* SCENE */
.scene {
  position: relative;
  width: 320px;
  height: 220px;
}

/* ENVELOPE */
.envelope {
  position: absolute;
  width: 100%;
  height: 100%;
  background: #fff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 20px 40px rgba(0,0,0,0.2);
  cursor: pointer;
  z-index: 2;
}

/* FLAP */
.flap {
  position: absolute;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #ff9aa2, #ffb7b2);
  clip-path: polygon(0 0, 100% 0, 50% 55%);
  transform-origin: top;
  transition: transform 1s ease;
  z-index: 3;
}

/* LETTER */
.letter {
  position: absolute;
  inset: 12px;
  background: #fffafc;
  border-radius: 6px;
  padding: 18px;
  line-height: 1.4;
  font-size: 14px;
  color: #444;
  transform: translateY(100%);
  transition: transform 1.2s ease;
  z-index: 1;
  overflow-y: auto;
}

/* OPEN ANIMATION */
#open:checked ~ .scene .flap {
  transform: rotateX(180deg);
}

#open:checked ~ .scene .letter {
  transform: translateY(0);
}

/* TAP HINT */
.hint {
  position: absolute;
  bottom: -45px;
  width: 100%;
  text-align: center;
  font-size: 13px;
  color: #6b0036;
  opacity: 0.8;
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0%,100% { opacity: .5; }
  50% { opacity: 1; }
}

/* PARTICLES */
.particles span {
  position: absolute;
  font-size: 20px;
  opacity: 0;
  animation: float 6s linear infinite;
}

#open:checked ~ .scene .particles span {
  opacity: 1;
}

@keyframes float {
  0% {
    transform: translateY(0) scale(0.6);
    opacity: 0;
  }
  20% { opacity: 1; }
  100% {
    transform: translateY(-500px) scale(1.2);
    opacity: 0;
  }
}

.particles span:nth-child(1) { left: 10%; animation-delay: 0s; }
.particles span:nth-child(2) { left: 30%; animation-delay: 1s; }
.particles span:nth-child(3) { left: 50%; animation-delay: 2s; }
.particles span:nth-child(4) { left: 70%; animation-delay: 3s; }
.particles span:nth-child(5) { left: 90%; animation-delay: 4s; }

/* HEARTS & FLOWERS */
.heart::before { content: "💗"; }
.flower::before { content: "🌸"; }
.flower2::before { content: "🌼"; }

/* 💐 BOUQUET POP EFFECT */
.bouquet {
  position: absolute;
  inset: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 70px;
  opacity: 0;
  transform: scale(0);
  transition: all 0.8s cubic-bezier(.68,-0.55,.27,1.55);
  z-index: 1;
  pointer-events: none;
}

#open:checked ~ .scene .bouquet {
  opacity: 1;
  transform: scale(1);
}

</style>
</head>
<body>

<input type="checkbox" id="open">

<label for="open" class="scene">

  <div class="bouquet">💐🌷🌹🌸</div>

  <div class="envelope">
    <div class="flap"></div>
    <div class="letter">
      <!DOCTYPE html>
<html>
<head>
<title>Falling Hearts</title>
<style>
body {
  background: #ffe6eb;
  overflow: hidden;
}

.heart {
  position: absolute;
  top: -50px;
  font-size: 30px;
  animation: fall 5s linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(110vh);
  }
}
</style>
</head>
<body>

<div class="heart" style="left:20%">❤️</div>
<div class="heart" style="left:50%; animation-delay:1s">💖</div>
<div class="heart" style="left:80%; animation-delay:2s">💘</div>

</body>
</html>

      Hi Golo, it’s me again. I know this is a little weird, but  
      I’ve been wanting to tell you that I like you since the very first time I saw you.  
      Your kindness, your smile, i like that hehe, and I'm not sure if you feel the same,
      but I just wanted to let you know. that I like you a lot. and i hope we can get to know each other better.
      and i really think that you are an amazing person., you are the type of a person that makes the world a better place just by being in it.
      i hope this message finds you well, and that you have a great day ahead.
      This isn’t meant to pressure you or expect anything.  
      I just wanted to be honest—because some feelings deserve  
      to be said at least once. and also i would like to you ask if would you like to recive something in valentines day? even if you says no, ill do it
      anyway hehe. just let me know. Take care always golochi! if you need anything, im here for you. 
      <br><br>
      
    </div>
  </div>

  <div class="particles">
    <span class="heart"></span>
    <span class="flower"></span>
    <span class="heart"></span>
    <span class="flower2"></span>
    <span class="heart"></span>
  </div>

  <div class="hint">Tap or click the letter 💌</div>
</label>

</body>
</html>
