<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Forgive Me Ginni ❤️</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: 'Poppins', sans-serif;
    }

    body{
      height:100vh;
      overflow:hidden;
      display:flex;
      justify-content:center;
      align-items:center;
      background: linear-gradient(135deg,#ff9a9e,#fad0c4,#fbc2eb);
      animation:bgMove 10s infinite alternate;
    }

    @keyframes bgMove{
      0%{filter:hue-rotate(0deg);}
      100%{filter:hue-rotate(25deg);}
    }

    .container{
      width:90%;
      max-width:700px;
      background:rgba(255,255,255,0.15);
      backdrop-filter:blur(12px);
      border-radius:25px;
      padding:40px;
      text-align:center;
      box-shadow:0 10px 40px rgba(0,0,0,0.2);
      animation:fadeIn 1.5s ease;
      position:relative;
    }

    @keyframes fadeIn{
      from{
        opacity:0;
        transform:translateY(40px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    h1{
      color:white;
      font-size:3rem;
      margin-bottom:20px;
      animation:heartbeat 2s infinite;
    }

    @keyframes heartbeat{
      0%{transform:scale(1);}
      25%{transform:scale(1.05);}
      50%{transform:scale(1);}
      75%{transform:scale(1.08);}
      100%{transform:scale(1);}
    }

    .message{
      color:white;
      font-size:1.2rem;
      line-height:1.8;
      margin-bottom:35px;
      animation:slideUp 1.5s ease;
    }

    @keyframes slideUp{
      from{
        opacity:0;
        transform:translateY(30px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    .question{
      color:white;
      font-size:1.8rem;
      margin-bottom:30px;
      font-weight:bold;
    }

    .buttons{
      position:relative;
      height:120px;
    }

    button{
      border:none;
      padding:15px 35px;
      font-size:1.2rem;
      border-radius:50px;
      cursor:pointer;
      transition:0.3s ease;
      font-weight:bold;
      position:absolute;
    }

    #yesBtn{
      background:#ff4d6d;
      color:white;
      left:35%;
      box-shadow:0 0 20px rgba(255,77,109,0.6);
    }

    #yesBtn:hover{
      transform:scale(1.1);
    }

    #noBtn{
      background:white;
      color:#ff4d6d;
      right:35%;
    }

    .final-message{
      display:none;
      margin-top:30px;
      animation:fadeLove 1s ease forwards;
    }

    @keyframes fadeLove{
      from{
        opacity:0;
        transform:scale(0.5);
      }
      to{
        opacity:1;
        transform:scale(1);
      }
    }

    .love{
      font-size:4rem;
      font-weight:bold;
      background:linear-gradient(to right,#ff0844,#ffb199);
      -webkit-background-clip:text;
      -webkit-text-fill-color:transparent;
      animation:glow 1.5s infinite alternate;
    }

    @keyframes glow{
      from{
        text-shadow:0 0 10px #fff;
      }
      to{
        text-shadow:0 0 30px #ff4d6d;
      }
    }

    .hearts{
      position:absolute;
      width:100%;
      height:100%;
      top:0;
      left:0;
      overflow:hidden;
      z-index:-1;
    }

    .heart{
      position:absolute;
      color:white;
      animation:float 8s linear infinite;
      opacity:0.7;
    }

    @keyframes float{
      from{
        transform:translateY(100vh) scale(0.5);
      }
      to{
        transform:translateY(-10vh) scale(1.5);
      }
    }

  </style>
</head>
<body>

<div class="hearts" id="hearts"></div>

<div class="container">

  <h1>I'm Sorry Ginni ❤️</h1>

  <div class="message">
    I know I made many mistakes in my past...<br><br>
    But trust me, I want to correct them all.<br>
    I don't want temporary moments with you...<br>
    I want forever. 🌸<br><br>
    You are genuinely special to me and I never want to lose you.
  </div>

  <div class="question">
    Do You Forgive Me? 🥺
  </div>

  <div class="buttons">
    <button id="yesBtn">Yes ❤️</button>
    <button id="noBtn">No 💔</button>
  </div>

  <div class="final-message" id="finalMessage">
    <h2 style="color:white;margin-bottom:20px;">
      I know tu mujhse jyada time gussa nhii reh skti ❤️
    </h2>

    <div class="love">
      LOVE YOU ✨
    </div>
  </div>

</div>

<script>

  const noBtn = document.getElementById("noBtn");
  const yesBtn = document.getElementById("yesBtn");
  const finalMessage = document.getElementById("finalMessage");

  let yesSize = 1;
  let noSize = 1;

  noBtn.addEventListener("click", () => {

    yesSize += 0.15;
    noSize -= 0.1;

    yesBtn.style.transform = `scale(${yesSize})`;
    noBtn.style.transform = `scale(${noSize})`;

    const x = Math.random() * 300 - 150;
    const y = Math.random() * 100 - 50;

    noBtn.style.transform += ` translate(${x}px, ${y}px)`;

    if(noSize <= 0.3){
      noBtn.style.display = "none";
    }
  });

  yesBtn.addEventListener("click", () => {
    finalMessage.style.display = "block";

    document.querySelector(".question").style.display = "none";
    document.querySelector(".buttons").style.display = "none";
  });

  // floating hearts

  const hearts = document.getElementById("hearts");

  for(let i=0;i<30;i++){

    const heart = document.createElement("div");
    heart.classList.add("heart");

    heart.innerHTML = "❤️";

    heart.style.left = Math.random()*100 + "vw";
    heart.style.fontSize = Math.random()*25 + 15 + "px";
    heart.style.animationDuration = Math.random()*5 + 5 + "s";

    hearts.appendChild(heart);
  }

</script>

</body>
</html>
