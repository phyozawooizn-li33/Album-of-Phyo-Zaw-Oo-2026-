<!DOCTYPE html>
<html lang="my">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Album of Phyo Zaw Oo (2026)</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #1e2430;
      color: #ffffff;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      overflow-x: hidden;
    }

    /* Header Section */
    .header {
      text-align: center;
      margin-bottom: 2rem;
      z-index: 10;
    }

    .header h1 {
      font-size: 2.2rem;
      letter-spacing: 2px;
      font-weight: 700;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .header .year-badge {
      background: rgba(255, 255, 255, 0.15);
      padding: 4px 16px;
      border-radius: 20px;
      font-size: 0.9rem;
      display: inline-block;
      color: #d1d5db;
    }

    /* 3D Book Flip Carousel Container */
    .carousel-container {
      position: relative;
      width: 100%;
      max-width: 1000px;
      height: 420px;
      perspective: 1200px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .book-card {
      position: absolute;
      width: 260px;
      height: 360px;
      border-radius: 16px;
      background-size: cover;
      background-position: center;
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
      transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1), opacity 0.6s, z-index 0.6s;
      cursor: pointer;
      overflow: hidden;
      border: 2px solid rgba(255, 255, 255, 0.1);
    }

    /* Glassmorphism Overlay (Album info like Music Player) */
    .card-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 15px;
      background: rgba(255, 255, 255, 0.2);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-top: 1px solid rgba(255, 255, 255, 0.3);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .card-info h3 {
      font-size: 1rem;
      font-weight: 600;
      color: #fff;
    }

    .card-info p {
      font-size: 0.8rem;
      color: #e0e0e0;
    }

    .play-btn {
      width: 36px;
      height: 36px;
      background: #222;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    }

    .play-btn svg {
      width: 16px;
      height: 16px;
      fill: #fff;
    }

    /* Navigation Buttons */
    .controls {
      margin-top: 2rem;
      display: flex;
      gap: 15px;
      z-index: 10;
    }

    .btn {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      border: none;
      background: rgba(255, 255, 255, 0.2);
      color: white;
      font-size: 1.2rem;
      cursor: pointer;
      backdrop-filter: blur(5px);
      transition: background 0.3s, transform 0.2s;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .btn:hover {
      background: rgba(255, 255, 255, 0.4);
      transform: scale(1.1);
    }

    /* 3D Positioning States for Book Flipping Effect */
    .book-card[data-pos="-2"] {
      transform: translateX(-240px) scale(0.75) rotateY(35deg);
      z-index: 1;
      opacity: 0.5;
    }

    .book-card[data-pos="-1"] {
      transform: translateX(-130px) scale(0.88) rotateY(20deg);
      z-index: 2;
      opacity: 0.8;
    }

    .book-card[data-pos="0"] {
      transform: translateX(0) scale(1.05) rotateY(0deg);
      z-index: 3;
      opacity: 1;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6);
    }

    .book-card[data-pos="1"] {
      transform: translateX(130px) scale(0.88) rotateY(-20deg);
      z-index: 2;
      opacity: 0.8;
    }

    .book-card[data-pos="2"] {
      transform: translateX(240px) scale(0.75) rotateY(-35deg);
      z-index: 1;
      opacity: 0.5;
    }

    .book-card[data-pos="hidden"] {
      transform: translateX(0) scale(0.5) rotateY(0deg);
      z-index: 0;
      opacity: 0;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <div class="header">
    <h1>Album of Phyo Zaw Oo</h1>
    <div class="year-badge">2026</div>
  </div>

  <!-- 3D Book Flip Carousel -->
  <div class="carousel-container" id="carousel">
    <!-- Card 1 -->
    <!-- GitHub တွင် တင်ထားသော ပုံ Link ကို url('...') ထဲတွင် ထည့်ပါ -->
    <div class="book-card" style="background-image: url('https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?w=500');">
      <div class="card-overlay">
        <div class="card-info">
          <h3>Track 01</h3>
          <p>Phyo Zaw Oo</p>
        </div>
        <div class="play-btn">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
        </div>
      </div>
    </div>

    <!-- Card 2 -->
    <div class="book-card" style="background-image: url('https://images.unsplash.com/photo-1470225620780-dba8ba36b745?w=500');">
      <div class="card-overlay">
        <div class="card-info">
          <h3>Track 02</h3>
          <p>Phyo Zaw Oo</p>
        </div>
        <div class="play-btn">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
        </div>
      </div>
    </div>

    <!-- Card 3 -->
    <div class="book-card" style="background-image: url('https://images.unsplash.com/photo-1514525253161-7a46d19cd819?w=500');">
      <div class="card-overlay">
        <div class="card-info">
          <h3>Track 03</h3>
          <p>Phyo Zaw Oo</p>
        </div>
        <div class="play-btn">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
        </div>
      </div>
    </div>

    <!-- Card 4 -->
    <div class="book-card" style="background-image: url('https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?w=500');">
      <div class="card-overlay">
        <div class="card-info">
          <h3>Track 04</h3>
          <p>Phyo Zaw Oo</p>
        </div>
        <div class="play-btn">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
        </div>
      </div>
    </div>

    <!-- Card 5 -->
    <div class="book-card" style="background-image: url('https://images.unsplash.com/photo-1459749411175-04bf5292ceea?w=500');">
      <div class="card-overlay">
        <div class="card-info">
          <h3>Track 05</h3>
          <p>Phyo Zaw Oo</p>
        </div>
        <div class="play-btn">
          <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
        </div>
      </div>
    </div>
  </div>

  <!-- Navigation Controls -->
  <div class="controls">
    <button class="btn" id="prevBtn">&#10094;</button>
    <button class="btn" id="nextBtn">&#10095;</button>
  </div>

  <script>
    const cards = document.querySelectorAll('.book-card');
    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');
    let currentIndex = 2; // စတင်ချိန်တွင် အလယ်ဗဟို၌ ပြသမည့် Card (Index 2)

    function updateCarousel() {
      cards.forEach((card, index) => {
        const offset = index - currentIndex;

        if (offset === 0) {
          card.setAttribute('data-pos', '0');
        } else if (offset === -1) {
          card.setAttribute('data-pos', '-1');
        } else if (offset === -2) {
          card.setAttribute('data-pos', '-2');
        } else if (offset === 1) {
          card.setAttribute('data-pos', '1');
        } else if (offset === 2) {
          card.setAttribute('data-pos', '2');
        } else {
          card.setAttribute('data-pos', 'hidden');
        }
      });
    }

    // Next / Prev ခလုတ်များ နှိပ်သည့်အခါ စာအုပ်လှန်သည့် အသွင်ပြောင်းလဲပေးခြင်း
    nextBtn.addEventListener('click', () => {
      if (currentIndex < cards.length - 1) {
        currentIndex++;
        updateCarousel();
      }
    });

    prevBtn.addEventListener('click', () => {
      if (currentIndex > 0) {
        currentIndex--;
        updateCarousel();
      }
    });

    // Card များကို နှိပ်၍လည်း တိုက်ရိုက် ရွေးချယ်နိုင်သည်
    cards.forEach((card, index) => {
      card.addEventListener('click', () => {
        currentIndex = index;
        updateCarousel();
      });
    });

    // စတင်ချိန်တွင် Carousel ကို Update လုပ်ပေးမည်
    updateCarousel();
  </script>
</body>
</html>
