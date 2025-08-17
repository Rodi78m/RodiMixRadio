# RodiMixRadio
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rodi Mix Radio</title>
<style>
body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f0e6d2; color:#333; text-align:center; }
header { background:#8B4513; color:white; padding:20px; }
.language-bar button { margin:5px; padding:10px 15px; border:none; background:#D2B48C; color:white; border-radius:5px; cursor:pointer; font-size:16px; }
iframe { width:100%; max-width:600px; height:166px; border:none; margin-top:20px; }
</style>
</head>
<body>
<header>
<h1>Rodi Mix Radio</h1>
<div class="language-bar">
<button onclick="switchLanguage('ku')">كردي</button>
<button onclick="switchLanguage('ar')">عربي</button>
<button onclick="switchLanguage('en')">English</button>
<button onclick="switchLanguage('de')">Deutsch</button>
</div>
</header>

<div id="player-container">
<iframe id="soundcloud-player" 
src="https://w.soundcloud.com/player/?url=https%3A//on.soundcloud.com/WDg2lQsOymnwTrNsa2&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"
allow="autoplay"></iframe>
</div>

<script>
const playlists = {
  ku: "https://on.soundcloud.com/WDg2lQsOymnwTrNsa2",
  ar: "https://on.soundcloud.com/bn6s08cf6T1b5m3qGo",
  en: "https://on.soundcloud.com/4usXz4ARvJ0cTz3niJ",
  de: "https://on.soundcloud.com/UmFzyC7QriTadJMUhp"
};

function switchLanguage(lang) {
  const player = document.getElementById('soundcloud-player');
  const url = encodeURIComponent(playlists[lang]);
  player.src = `https://w.soundcloud.com/player/?url=${url}&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true`;
}
</script>
</body>
</html>


