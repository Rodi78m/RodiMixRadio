# RodiMixRadio
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>محطة راديو Rodi Mix</title>
  <style>
    body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f0e6d2; color:#333; text-align:center; }
    header { background:#8B4513; color:white; padding:20px; }
    .language-bar button { margin:0 5px; padding:10px 15px; border:none; background:#D2B48C; color:white; border-radius:5px; cursor:pointer; font-size:16px; }
    .player-container iframe { width:100%; height:166px; border:none; margin:20px 0; }
    footer { background:#8B4513; color:white; padding:10px; }
  </style>
</head>
<body>
  <header>
    <h1>محطة راديو Rodi Mix</h1>
    <div class="language-bar">
      <button onclick="switchLanguage('ar')">العربية</button>
      <button onclick="switchLanguage('ku')">كردي</button>
      <button onclick="switchLanguage('en')">English</button>
      <button onclick="switchLanguage('de')">Deutsch</button>
    </div>
  </header>
  
  <div id="player-container"></div>
  
  <footer>&copy; 2025 Rodi Mix Radio</footer>
  
  <script>
    const players = {
      ar: "https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/trackistador/sets/arabic-egyptian-oriental-music-free-to-use-creative-commons&color=%23ff5500&auto_play=false",
      ku: "https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/younes-mohammad/sets/kurdish&color=%23ff5500&auto_play=false",
      en: "https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/aamir-khan-53/sets/best-english-songs-2021&color=%23ff5500&auto_play=false",
      de: "https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/trackistador/sets/german-music-deutsche-musik-free-to-use-creative-commons&color=%23ff5500&auto_play=false"
    };
  
    function switchLanguage(lang) {
      document.getElementById('player-container').innerHTML = `
        <iframe scrolling="no" frameborder="no" src="${players[lang]}"></iframe>`;
    }
  
    window.onload = () => switchLanguage('ar');
  </script>
</body>
</html>

