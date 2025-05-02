
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>For Kei & Ale - My Best Friends</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&family=Dancing+Script&display=swap');

  /* Reset */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #f0e4f7, #c9d6ff);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 2rem 1rem;
    color: #222;
    overflow-x: hidden;
    position: relative;
  }

  .container {
    max-width: 730px;
    background: white;
    border-radius: 25px;
    box-shadow: 0 15px 30px rgba(0,0,0,0.15);
    padding: 2.5rem 3rem;
    position: relative;
    overflow: hidden;
    z-index: 10;
  }

  h1 {
    font-family: 'Dancing Script', cursive;
    font-size: 3.5rem;
    color: #8a2be2;
    margin-bottom: 0.25rem;
    user-select: none;
    text-align: center;
    text-shadow: 1px 1px 6px rgba(138,43,226,0.3);
  }

  h2 {
    font-weight: 600;
    font-size: 1.8rem;
    color: #6a4c93;
    text-align: center;
    margin-bottom: 1.8rem;
  }

  p {
    font-weight: 300;
    font-size: 1.15rem;
    line-height: 1.75;
    margin-bottom: 1.25rem;
    padding-left: 0.4rem;
  }

  p:last-of-type {
    padding-left: 0;
  }

  /* Decorative floating shapes */
  .decor {
    position: absolute;
    border-radius: 50%;
    opacity: 0.15;
    filter: drop-shadow(0 0 3px rgba(138,43,226,0.15));
    animation: floatUpDown 6s ease-in-out infinite alternate;
  }

  .decor1 {
    width: 140px;
    height: 140px;
    background: #b294f9;
    top: -40px;
    left: -40px;
    animation-delay: 0s;
  }

  .decor2 {
    width: 90px;
    height: 90px;
    background: #d4b5f9;
    bottom: -30px;
    right: -30px;
    animation-delay: 3s;
  }

  .decor3 {
    width: 70px;
    height: 70px;
    background: #c4a1f3;
    top: 150px;
    right: 20px;
    animation-delay: 1.5s;
  }

  @keyframes floatUpDown {
    from {
      transform: translateY(0);
    }
    to {
      transform: translateY(15px);
    }
  }

  /* Additional Decorations */

  /* Stars */
  .star {
    position: absolute;
    width: 15px;
    height: 15px;
    background: linear-gradient(45deg, #ffecb3, #ffc107);
    clip-path: polygon(
      50% 0%,
      61% 35%,
      98% 35%,
      68% 57%,
      79% 91%,
      50% 70%,
      21% 91%,
      32% 57%,
      2% 35%,
      39% 35%
    );
    opacity: 0.7;
    animation: twinkle 4s ease-in-out infinite alternate;
  }

  /* Hearts */
  .heart {
    position: absolute;
    width: 20px;
    height: 18px;
    background-color: #e75480;
    transform: rotate(-45deg);
    animation: floatUp 6s linear infinite;
    opacity: 0.8;
    border-radius: 20px 20px 0 0;
    filter: drop-shadow(0 0 2px #e75480);
  }
  .heart::before,
  .heart::after {
    content: "";
    position: absolute;
    width: 20px;
    height: 18px;
    background-color: #e75480;
    border-radius: 50%;
    top: 0;
    left: 0;
  }
  .heart::before {
    left: 10px;
  }
  .heart::after {
    top: -9px;
    left: 5px;
  }

  @keyframes floatUp {
    0% {
      transform: translateY(0) rotate(-45deg);
      opacity: 0.8;
    }
    50% {
      opacity: 1;
    }
    100% {
      transform: translateY(-120px) rotate(-45deg);
      opacity: 0;
    }
  }

  /* Confetti */
  .confetti {
    position: absolute;
    width: 8px;
    height: 14px;
    background-color: #ff6f91;
    opacity: 0.85;
    transform-origin: center center;
    border-radius: 2px;
    animation: confettiFall linear infinite forwards;
  }
  .confetti:nth-child(1) { left: 10%; animation-duration: 6s; animation-delay: 0s; background-color: #ff6f91;}
  .confetti:nth-child(2) { left: 20%; animation-duration: 8s; animation-delay: 1s; background-color: #f9a1bc;}
  .confetti:nth-child(3) { left: 30%; animation-duration: 5s; animation-delay: 1.5s; background-color: #fbc1cc;}
  .confetti:nth-child(4) { left: 40%; animation-duration: 7s; animation-delay: 2s; background-color: #d6a4dd;}
  .confetti:nth-child(5) { left: 50%; animation-duration: 6.5s; animation-delay: 2.5s; background-color: #b294f9;}
  .confetti:nth-child(6) { left: 60%; animation-duration: 7.5s; animation-delay: 3s; background-color: #a2c1e3;}
  .confetti:nth-child(7) { left: 70%; animation-duration: 8.5s; animation-delay: 3.5s; background-color: #8ac6d1;}
  .confetti:nth-child(8) { left: 80%; animation-duration: 9s; animation-delay: 4s; background-color: #feeece;}
  .confetti:nth-child(9) { left: 90%; animation-duration: 8s; animation-delay: 4.5s; background-color: #f9a1bc;}

  @keyframes confettiFall {
    0% {
      transform: translateY(-20px) rotate(0deg);
      opacity: 1;
    }
    100% {
      transform: translateY(600px) rotate(360deg);
      opacity: 0;
    }
  }

  /* Twinkle Animation */
  @keyframes twinkle {
    0%, 100% { opacity: 0.7; transform: scale(1) rotate(0deg);}
    50% { opacity: 1; transform: scale(1.2) rotate(20deg);}
  }

  /* Responsive */
  @media (max-width: 480px) {
    .container {
      padding: 1.5rem 1.5rem;
      max-width: 95vw;
    }
    h1 {
      font-size: 2.5rem;
    }
    h2 {
      font-size: 1.4rem;
      margin-bottom: 1.2rem;
    }
    p {
      font-size: 1rem;
      padding-left: 0;
    }
  }
</style>
</head>
<body>
  <!-- Confetti decorations -->
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>
  <div class="confetti" aria-hidden="true"></div>

  <!-- Floating stars and hearts -->
  <div class="star" style="top: 20px; left: 15px; animation-delay: 0s;"></div>
  <div class="star" style="top: 140px; right: 40px; animation-delay: 1.5s;"></div>
  <div class="star" style="top: 180px; left: 60px; animation-delay: 3s;"></div>
  <div class="star" style="top: 90px; right: 110px; animation-delay: 4.5s;"></div>
  <div class="star" style="top: 30px; left: 250px; animation-delay: 6s;"></div>
  
  <div class="heart" style="bottom: 60px; left: 50px; animation-delay: 0s; animation-duration: 5s;"></div>
  <div class="heart" style="bottom: 100px; right: 70px; animation-delay: 2s; animation-duration: 6s; width: 24px; height: 22px;"></div>
  <div class="heart" style="bottom: 40px; right: 150px; animation-delay: 4s; animation-duration: 5.5s;"></div>
  <div class="heart" style="top: 10px; right: 220px; animation-delay: 1s; animation-duration: 7s; width: 18px; height: 16px;"></div>
  <div class="heart" style="bottom: 130px; left: 210px; animation-delay: 3s; animation-duration: 5.8s;"></div>

  <div class="container" role="main" aria-label="Tribute message to best friends Kei and Ale">
    <h1>Kei & Ale</h1>
    <h2>My Dearest Best Friends</h2>
    <p>From the moment we met, it felt like destiny wrapped in the brightest colors of friendship. Kei, your laughter is a melody that lightens even the heaviest days, and Ale, your kindness is a warm embrace that makes this world a better place. Together, you both create a harmony of joy, comfort, and inspiration that has touched my heart in ways words can barely express.</p>
    <p>Through the countless memories we've shared — the endless conversations into the night, the spontaneous adventures filled with excitement, the quiet moments of understanding when no words were needed — you have shown me the true meaning of companionship. Your unwavering support, your honesty, and your unique sparks of brilliance make you not just friends, but family.</p>
    <p>Kei, your fierce determination and creativity inspire me daily to chase my dreams without hesitation. Ale, your gentle spirit and endless compassion teach me the power of empathy and grace. You both balance each other perfectly, and I'm grateful to witness the beautiful dynamic between you.</p>
    <p>As we continue this journey, I cherish every laugh, every tear, and every moment that we grow closer together. I look forward to celebrating countless milestones, sharing endless joy, and standing by your side through every challenge life throws at us.</p>
    <p>This website is a small token of appreciation, a place to honor the incredible friendship and love that you both bring into my life and the lives of everyone lucky enough to know you.</p>
    <p>Thank you, Kei and Ale, for being the wonderful souls you are. Here's to today, tomorrow, and every beautiful day after. Forever your friend and biggest fan.</p>
    <p style="font-weight: bold; text-align: center; margin-top: 2rem;">With all my heart, <br />Your Best Friend</p>

    <div class="decor decor1" aria-hidden="true"></div>
    <div class="decor decor2" aria-hidden="true"></div>
    <div class="decor decor3" aria-hidden="true"></div>
  </div>
</body>
</html>
