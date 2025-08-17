# RodiMixRadio
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rodi Mix Radio</title>
<style>
body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f0e6d2; color: #333; }
header { background: #8B4513; color: white; padding: 20px; text-align: center; }
.language-bar button { margin: 0 5px; padding: 5px 10px; border: none; background: #D2B48C; color: white; border-radius: 5px; cursor: pointer; }
.radio-section { padding: 20px; text-align: center; }
iframe { width: 100%; height: 166px; border: none; }
footer { position: fixed; bottom: 0; width: 100%; background: #8B4513; color: white; padding: 10px; text-align: center; }
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

<div class="radio-section">
<div id="radio-player">
<iframe src="https://on.soundcloud.com/WDg2lQsOymnwTrNsa2" allow="autoplay"></iframe>
</div>
</div>

<footer>
<p>Rodi Mix Radio - كل الحقوق محفوظة</p>
</footer>

<script>
let radios = {
  ku: "https://on.soundcloud.com/WDg2lQsOymnwTrNsa2",
  ar: "https://on.soundcloud.com/bn6s08cf6T1b5m3qGo",
  en: "https://on.soundcloud.com/4usXz4ARvJ0cTz3niJ",
  de: "https://on.soundcloud.com/UmFzyC7QriTadJMUhp"
};

function switchLanguage(lang) {
  document.getElementById('radio-player').innerHTML = `<iframe src="${radios[lang]}" allow="autoplay"></iframe>`;
}
</script>
</body>
</html>
