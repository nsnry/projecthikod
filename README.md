# projecthikod

<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dizi & Film Öneri Sitesi</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #0e0e10;
      color: #e5e5e5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      position: relative;
      overflow-x: hidden;
    }

    header {
      background: #1c1c1e;
      color: #fff;
      padding: 2rem 1rem;
      text-align: center;
      border-bottom: 2px solid #333;
      z-index: 10;
    }

    header h1 {
      font-size: 2.8rem;
      font-weight: 700;
    }

    .background-gallery {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      overflow: hidden;
    }

    .background-gallery img {
      position: absolute;
      width: 200px;
      height: auto;
      opacity: 0.08;
      transform: rotate(-15deg);
      object-fit: cover;
      border-radius: 12px;
    }

    .container {
      flex: 1;
      max-width: 900px;
      margin: 4rem auto;
      padding: 2rem;
      background: rgba(30, 30, 33, 0.95);
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.7);
      z-index: 1;
      position: relative;
    }

    .btn {
      background: #ff3d00;
      color: white;
      padding: 0.8rem 1.6rem;
      font-size: 1.1rem;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: 500;
      margin-bottom: 2rem;
      transition: background 0.3s ease, transform 0.2s ease;
    }

    .btn:hover {
      background: #e53700;
      transform: scale(1.05);
    }

    .recommendation {
      background-color: #2a2a2e;
      padding: 2rem;
      border-radius: 12px;
      font-size: 1.2rem;
      color: #fff;
      font-weight: 500;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
      animation: fadeIn 0.5s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <header>
    <h1>🎥 Dizi & Film Öneri Kutusu</h1>
    <p>Favori karakterlerle ilham al, yeni yapımlarla keşfe çık!</p>
  </header>

  <div class="background-gallery">
    <img src="dizifilm1.jpg" style="top: 50px; left: 20px;">
    <img src="dizifil3.jpg" style="top: 100px; left: 300px;">
    <img src="dizifilm44.jpg" style="top: 250px; left: 100px;">
    <img src="dizifil5.jpg" style="top: 400px; left: 500px;">
    <img src="dizi6.jpg" style="top: 200px; left: 1000px;">
    <img src="di7.jpg" style="top: 400px; left: 90px;">
    <img src="d8.jpg" style="top: 100px; left: 900px;">
    <img src="d9.jpg" style="top: 250px; left: 400px;">
    <img src="d10.jpg" style="top: 100px; left: 500px;">
    <img src="d1.jpg" style="top: 5%; left: 300px;">
  </div>

  <div class="container">
    <button class="btn" onclick="getRecommendation()">🍿 Bana bir öneri ver</button>
    <div id="recommendation" class="recommendation"></div>
  </div>

  <script>
    const suggestions = [
      "🎬 Breaking Bad - Suç, Dram, Gerilim",
      "😂 Friends - Komedi, Sitcom",
      "👾 Stranger Things - Bilim Kurgu, Gerilim",
      "📂 The Office - Komedi, İş Hayatı",
      "🌀 Dark - Gizem, Bilim Kurgu",
      "🕵️ Sherlock - Polisiye, Gizem",
      "🚀 Interstellar - Bilim Kurgu, Macera",
      "🧠 Inception - Bilim Kurgu, Aksiyon",
      "💰 La Casa de Papel - Suç, Aksiyon",
      "👑 The Crown - Tarihi, Dram"
    ];

    function getRecommendation() {
      const randomIndex = Math.floor(Math.random() * suggestions.length);
      const recommendationDiv = document.getElementById('recommendation');
      recommendationDiv.innerText = suggestions[randomIndex];
    }
  </script>
</body>
</html>

  
