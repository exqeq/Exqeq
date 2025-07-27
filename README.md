<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>exqeq - Visual Artist</title>
  <link href="https://fonts.googleapis.com/css2?family=Merriweather&family=Playfair+Display&display=swap" rel="stylesheet" />
  <style>
    /* Reset & base */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body, html {
      height: 100%;
      font-family: 'Merriweather', serif;
      color: #f0f0f0;
      background: #001d3d;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }
    a {
      color: #9dd9f3;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #ffe066;
    }

    /* Section container */
    section {
      min-height: 100vh;
      padding: 3rem 2rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      z-index: 2;
    }

    /* Overlay backgrounds */
    .bg-otter {
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      position: fixed;
      top:0; left:0; width: 100%; height: 100%;
      filter: brightness(0.4) saturate(1.3);
      z-index: 0;
      transition: background 1s ease;
    }
    .bg-palms {
      background: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1471&q=80') no-repeat center center/cover;
      position: fixed;
      top:0; left:0; width: 100%; height: 100%;
      opacity: 0;
      filter: brightness(0.6) saturate(1.2);
      z-index: 0;
      transition: opacity 1.5s ease;
    }
    .show-palms {
      opacity: 1;
    }
    /* Transparent overlay for treasure map */
    .bg-treasure {
      background: url('https://images.unsplash.com/photo-1500534623283-312aade485b7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      position: fixed;
      top:0; left:0; width: 100%; height: 100%;
      opacity: 0;
      filter: brightness(0.25);
      z-index: 0;
      transition: opacity 1.5s ease;
    }
    .show-treasure {
      opacity: 1;
    }

    /* First hero text */
    h1#exqeq {
      font-family: 'Playfair Display', serif;
      font-size: 6rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      margin-bottom: 0.3rem;
      opacity: 0;
      animation: fadeInUp 2s forwards 0.5s;
      color: #a7d8f7;
      text-shadow: 0 0 10px #70b9ffcc;
    }
    h2#visual-artist {
      font-family: 'Playfair Display', serif;
      font-size: 2.5rem;
      font-weight: 400;
      color: #d0e8ffcc;
      opacity: 0;
      animation: fadeInUp 2s forwards 1.5s;
      letter-spacing: 0.15em;
      margin-bottom: 0;
      text-shadow: 0 0 6px #60aaffcc;
    }

    /* Biography and Works text */
    .content-text {
      max-width: 700px;
      font-size: 1.25rem;
      line-height: 1.7;
      margin-top: 3rem;
      color: #d8eefe;
      font-weight: 300;
      opacity: 0;
      animation: fadeIn 2s forwards 2.5s;
      text-align: left;
      background: rgba(0, 30, 60, 0.6);
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 0 15px #228be6aa;
    }
    /* Footer treasure locked */
    footer {
      height: 100vh;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      color: #ffc857;
      text-shadow: 0 0 15px #ffb100cc;
      z-index: 2;
      padding: 2rem;
    }
    footer .locked-key {
      position: absolute;
      bottom: 30%;
      width: 120px;
      opacity: 0.85;
      filter: drop-shadow(0 0 5px #ffb100cc);
      animation: float 4s ease-in-out infinite;
      user-select: none;
      pointer-events: none;
    }

    /* Animations */
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(40px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    @keyframes fadeIn {
      0% {opacity: 0;}
      100% {opacity: 1;}
    }
    @keyframes float {
      0%, 100% {transform: translateY(0);}
      50% {transform: translateY(-15px);}
    }
  </style>
</head>
<body>

  <div class="bg-otter" id="bgO"></div>
  <div class="bg-palms" id="bgP"></div>
  <div class="bg-treasure" id="bgT"></div>

  <section id="hero">
    <h1 id="exqeq">exqeq</h1>
    <h2 id="visual-artist">Visual Artist</h2>
  </section>

  <section id="bio">
    <div class="content-text">
      <h3>About Me</h3>
      <p>
        A quiet soul with deep oceans inside, exqeq captures feelings rather than just images.
        His photography and videography are a journey through light, shadow, and emotion.
        Creator of EQUXZERKA — a tropical luxury brand born from dreams and the sea.
      </p>
      <p>
        He builds worlds through art, technology, and storytelling — blending AI, design, and human connection.
        With a gentle spirit and a fierce vision, he moves slow, feels deep, and creates timeless beauty.
      </p>
    </div>
  </section>

  <section id="works">
    <div class="content-text">
      <h3>What I Do</h3>
      <ul style="list-style-type: square; margin-left: 1.5rem; font-weight: 400;">
        <li>Photography & Videography — portraits, landscapes, and cinematic storytelling</li>
        <li>High-end Tropical Fashion Brand — EQUXZERKA</li>
        <li>Luxury Tech Brand — LEMBEHAR | Noir</li>
        <li>AI Chatbot & Voice Assistants — helping businesses communicate with soul</li>
        <li>Author — writing books of mental escape and soul journeys</li>
        <li>Future vision — building peaceful tropical homes and a secret museum of stories</li>
      </ul>
    </div>
  </section>

  <footer>
    <div>🔒 Treasure Locked — Discover the Story</div>
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/34/Gold_Key_icon.svg/120px-Gold_Key_icon.svg.png"
      alt="Golden Key"
      class="locked-key"
    />
  </footer>

  <script>
    // Scroll effect to swap backgrounds
    window.addEventListener('scroll', () => {
      const palmsBg = document.getElementById('bgP');
      const treasureBg = document.getElementById('bgT');
      const scrollPos = window.scrollY;
      const windowHeight = window.innerHeight;

      if(scrollPos > windowHeight * 0.5) {
        palmsBg.classList.add('show-palms');
      } else {
        palmsBg.classList.remove('show-palms');
      }

      if(scrollPos > windowHeight * 2) {
        treasureBg.classList.add('show-treasure');
      } else {
        treasureBg.classList.remove('show-treasure');
      }
    });
  </script>

</body>
</html>
