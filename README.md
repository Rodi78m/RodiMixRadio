<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rodi Mix Radio</title>
<style>
body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f0e6d2; color: #333; }
header { background: #8B4513; color: white; padding: 20px; text-align: center; }
.language-bar button { margin: 0 5px; padding: 5px 10px; border: none; background: #D2B48C; color: white; border-radius: 5px; cursor: pointer; }
.song-section { padding: 20px; text-align:center; }
iframe { margin: 10px 0; border-radius:10px; }
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

<div class="song-section" id="song-section">
<!-- Embed will load here -->
</div>

<script>
const embeds = {
  ku: '<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/hedar-hussein/sets/kurdish-music&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  ar: '<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/bn6s08cf6t1b5m3qgo&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  en: '<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/4usxz4arvj0ctz3nij&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>',
  de: '<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/umfzyc7qritadjmuhp&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>'
};

function switchLanguage(lang) {
  document.getElementById('song-section').innerHTML = embeds[lang];
}

// Load default language
switchLanguage('ku');
</script>

</body>
</html>
