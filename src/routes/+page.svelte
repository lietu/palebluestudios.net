<script lang="ts">
  import PBSLogo from '$lib/assets/PBS_-_Logo.svg';

  const starChildUrl = 'https://store.steampowered.com/app/2953070/Star_Child/?utm_source=homepage&utm_medium=organic';
  const toleoUrl = 'https://store.steampowered.com/app/2312780/Toleo/?utm_source=homepage&utm_medium=organic';
</script>

<div class="logo">
  <PBSLogo />
</div>

<h1>What is Pale Blue Studios?</h1>
<p>We're a small indie game studio.</p>

<h2>Star Child</h2>
<p>
  Star Child is an explosive new action-adventure set on a sinister alien planet. Fight numerous aliens and formidable
  bosses, wield powerful explosives and destructive laser weapons, find secrets and unlock new abilities as you
  progress. Can you survive your dangerous mission? Currently in-progress, wishlist Star Child on <a
  href={starChildUrl}>Steam</a>.
</p>
<p>Check out the <a href="/presskit/starchild/">Press kit</a>.</p>

<p>Dev Logs</p>
<ul>
  <li><a href="https://store.steampowered.com/news/app/2953070/view/500571481680380399" target="_blank">Star Child Dev Log #1</a></li>
  <li><a href="https://store.steampowered.com/news/app/2953070/view/500572113230365186" target="_blank">Star Child Dev Log #2</a></li>
</ul>

<a href={starChildUrl}><img src="/starchild/starchild-header.jpg" alt="Wishlist Star Child on Steam" /></a>

<h2>Toleo</h2>
<p>Toleo is a fast, fluid and fun pixel-art precision platformer. Run, jump, slide, and flap your way through beautiful,
  hand-crafted worlds. Toleo is now available on <a href={toleoUrl}>Steam</a>.</p>
<a href={toleoUrl}><img src="/toleo/toleo-header.jpg" alt="Check out Toleo on Steam" /></a>

<h2>How to find us</h2>
<p>You can find us on various social media</p>
<ul>
  <li><a href="https://bsky.app/profile/palebluestudios.net">Bluesky</a></li>
  <li><a href="https://x.com/palebluetx">Twitter</a></li>
  <li><a href="https://www.reddit.com/user/PaleBlueStudios/">Reddit</a></li>
  <li><a href="https://twitch.tv/palebluecamel">Twitch (PaleBlueCamel)</a></li>
  <li><a href="https://www.tiktok.com/@pale.blue.studios">TikTok</a></li>
</ul>

<h2>Other presence</h2>
<p>You can find more about us also on</p>
<ul>
  <li><a href="https://www.indiedb.com/company/pale-blue-studios">IndieDB</a></li>
</ul>

<h2>Press kits</h2>
<ul>
  <li><a href="/presskit/starchild/">Star Child</a></li>
</ul>

<style lang="scss">
  .logo {
    display: flex;
    flex-direction: row;

    :global(svg) {
      margin: auto;
      fill: #1e8bd7;
      max-width: 24rem;
    }
  }

</style>
