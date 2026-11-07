---
layout: game
game: oopsbloom
title: "Oopsbloom: Cozy Climbing Game"
description: Fall today. Bloom tomorrow. A cozy one-thumb climbing game where every fall leaves a seed that blooms into a plant to help you climb.
image: /oopsbloom/og-image.png
---

## About the game

Fall today. Bloom tomorrow. Hold to charge, let go to jump, and help Sprout, a tiny seedling, climb a tall pixel cliff. Miss a ledge and you tumble down, but every fall leaves a glowing seed in the gap you missed. Eight real hours later it blooms right there, so the gap that stopped you yesterday can carry you today.

## Features

- **Four plants that help you climb:** a vine to grab, a mushroom that bounces you up, a dandelion that floats you back to your ledge, and a sunflower that becomes a new starting point.
- **A cliff that is yours alone.** It stays the same, so your garden becomes a map of every place you have fallen.
- **A camp every ten ledges**, each with a short letter from the one who climbed before you.
- **New zones higher up:** wind that pushes your jumps, ledges that crumble and ledges of ice.
- **Short climbs for short breaks**, with no lives and no energy to wait for.
- **Plays offline, no account needed.** Ads only appear between climbs, and rewarded ads are always your choice.

{% assign g = site.data.games | where: "id", "oopsbloom" | first %}{% if g.play_url and g.play_url != "" %}
<script>
// The in-game share card links here; its text adds ?s=<share spot>.
// Printed only when play_url is set. No redirect on iPhone/iPad or when coming from this website, so the page stays readable.
(function () {
  if (/iPhone|iPad|iPod/.test(navigator.userAgent)) return;
  if (document.referrer.indexOf(location.origin + '/') === 0) return;
  var OK = ['station', 'garden', 'dawn', 'season', 'gap'];
  var s = new URLSearchParams(location.search).get('s');
  var ref = 'utm_source=share&utm_medium=' + (OK.indexOf(s) >= 0 ? s : 'other') + '&utm_campaign=organic_share';
  location.replace('https://play.google.com/store/apps/details?id=com.playvyngames.oopsbloom&referrer=' + encodeURIComponent(ref));
})();
</script>
{% endif %}
