---
layout: game
game: duskbanner
title: Duskbanner
description: Lead a hero and a growing army through endless nights of monster hordes. A pixel-art survivors-like for Android by PlayVyn Games.
image: /duskbanner/og-image.png
---

## About the game

Night falls and the horde never stops. Move with one thumb while your weapons attack on their own, recruit an army to fight at your side, and pick an upgrade every level to build a different run each time. Hold out until dawn.

## Features

- **Nine heroes**, each with their own starting weapon, ultimate and play style.
- **Recruit an army**: swordsmen, spearmen, archers, guardians and clerics fight beside you.
- **Weapon evolutions**: pair a maxed weapon with the right item to unlock a stronger form.
- **Five maps and bosses** with their own skills, plus Night levels for extra challenge.
- **Short runs** for a quick break, full nights when you have time.
- **Plays offline.** Ads are optional rewarded ads only: you choose when to watch one.

{% assign g = site.data.games | where: "id", "duskbanner" | first %}{% if g.play_url and g.play_url != "" %}
<script>
// In-game share links (Duskbanner 1.0.4+) add ?s=<spot>. Only those links go straight to Google Play, with a UTM referrer.
// No ?s= -> normal page. No redirect on iPhone/iPad (including iPadOS desktop mode) or when coming from this website.
(function () {
  var s = new URLSearchParams(location.search).get('s');
  if (s === null) return;
  if (/iPhone|iPad|iPod/.test(navigator.userAgent)) return;
  if (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1) return;
  if (document.referrer.indexOf(location.origin + '/') === 0) return;
  var OK = ['record', 'win', 'run'];
  var ref = 'utm_source=share&utm_medium=' + (OK.indexOf(s) >= 0 ? s : 'other') + '&utm_campaign=organic_share';
  location.replace('{{ g.play_url }}&referrer=' + encodeURIComponent(ref));
})();
</script>
{% endif %}
