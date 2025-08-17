<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rodi Mix Radio</title>
<style>
body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f0e6d2; color:#333; text-align:center; }
header { background:#8B4513; color:white; padding:20px; }
.language-bar button { margin:5px; padding:10px 15px; border:none; border-radius:5px; background:#D2B48C; color:white; cursor:pointer; }
iframe { width:100%; height:166px; border:none; margin-top:20px; border-radius:10px; }
</style>
</head>
<body>
<header>
<h1>Rodi Mix Radio</h1>
<div class="language-bar">
<button onclick="switchLanguage('ar')">العربية</button>
<button onclick="switchLanguage('ku')">كردي</button>
<button onclick="switchLanguage('en')">English</button>
<button onclick="switchLanguage('de')">Deutsch</button>
</div>
</header>

<div id="player-container">
<!-- مشغل SoundCloud سيظهر هنا -->
</div>

<script>
const players = {
  ar: '<iframe scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//on.soundcloud.com/bn6s08cf6T1b5m3qGo&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  ku: '<iframe scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//on.soundcloud.com/WDg2lQsOymnwTrNsa2&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  en: '<iframe scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//on.soundcloud.com/4usXz4ARvJ0cTz3niJ&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  de: '<iframe scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//on.soundcloud.com/UmFzyC7QriTadJMUhp&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>'
};

function switchLanguage(lang){
  document.getElementById('player-container').innerHTML = players[lang];
}

// التشغيل الافتراضي عند فتح الصفحة
switchLanguage('ar');
</script>
</body>
</html>

