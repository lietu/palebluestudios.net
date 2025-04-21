<script lang="ts">
  import PressKit from '$lib/assets/PressKit.svelte';
  import Img from '$lib/assets/Img.svelte';
  import Svg from '$lib/assets/Svg.svelte';
  import StarChildTransparentLogo from '$lib/assets/starchild/starchild-transparent-logo.svg';

  const links = {
    Steam: 'https://store.steampowered.com/app/2953070/Star_Child/?utm_source=homepage&utm_medium=organic',
    IndieDB: 'https://www.indiedb.com/games/star-child1',
    'Gameplay Preview (April 2025)': 'https://www.youtube.com/watch?v=oGBFaiw5itM',
    'Gameplay Preview - Vertical (April 2025)': 'https://youtube.com/shorts/gLaZf0wY_cQ',
    'Banner .psd': '/starchild/starchild-banner.psd'
  };
</script>

<PressKit links={links}>
  {#snippet name()}Star Child{/snippet}
  {#snippet trailer()}
    <iframe src="https://www.youtube.com/embed/oGBFaiw5itM?si=AMThfVoSsnwJRLsu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  {/snippet}
  {#snippet description()}
    Star Child is a sci-fi pixel-art metroidvania that tries to honor the classics of the genre, while refining on some aspects.
  {/snippet}
  {#snippet history()}
    <p>
      In July 2023 we started planning new games, after some thinking we decided on Star Child being the next game to
      focus on. We started work in August 2023 by listing the basic concepts we'd want to see in the game, and the main
      inspirations.
    </p>
    <p>
      One of the obvious inspirations has been the original Metroid on the NES, but we also drew inspirations from the
      likes of Xeodrifter, Celeste, Axiom Verge, and Wings of Vi. Also Animal Well has served as a great reminder of how
      much relatively simple pixel animations can really add to the feeling of a game, we're really trying to learn from
      that.
    </p>
    <p>
      Pretty much immediately we knew we'd want <a href="https://www.tantrumtech.dev" target="_blank" rel="noopener">Tantrum Tech</a>
      to make the OST and sfx for this game as well, as they already did a great job with our previous game, <a
      href="https://store.steampowered.com/app/2312780/Toleo/?utm_source=homepage&utm_medium=organic&utm_campaign=social"
      target="_blank" rel="noopener">Toleo</a>.
    </p>
    <p>
      We really wanted the movement, traversal, and combat all to be fast and fluid. The world has an air of sinister
      mystery. The bosses are challenging imaginative spectacles. The music pushes you forward into the challenges,
      encouraging you while warning you.
    </p>
  {/snippet}
  {#snippet release_date()}
    We're hoping to release in 2025, but are not committed to it yet.
  {/snippet}
  {#snippet pricing()}
    Our target price is $20 USD.
  {/snippet}
  {#snippet platforms()}
    We want to launch on Steam and Itch.io, supporting Windows and Linux, possibly also Mac.
  {/snippet}
  {#snippet contact()}
    <ul>
      <li>Email: <a href="mailto:palebluetx@gmail.com">palebluetx@gmail.com</a></li>
    </ul>
  {/snippet}
  {#snippet features()}
    <ul>
      <li>Fast and fluid movement, traversal, and combat.</li>
      <li>Colorful, hand-crafted pixel-art.</li>
      <li>Full keyboard and controller support.</li>
      <li>Explore, conquer, and escape from a distant alien planet.</li>
      <li>Fight numerous aliens and formidable bosses.</li>
      <li>Wield powerful explosives and destructive laser weapons.</li>
      <li>Find numerous secrets and powerup items.</li>
      <li>Multiple difficulties and a variety of gameplay modes.</li>
      <li>This game is for all ages and will be designed for players of all skill levels.</li>
      <li>Fully original soundtrack by Tantrum Tech</li>
    </ul>
  {/snippet}
  {#snippet screenshots()}
    <Img src="/starchild/starchild-screenshot-1.png" />
    <Img src="/starchild/starchild-screenshot-2.png" />
    <Img src="/starchild/starchild-screenshot-3.png" />
    <Img src="/starchild/starchild-screenshot-4.png" />
    <Img src="/starchild/starchild-screenshot-5.png" />
    <Img src="/starchild/starchild-screenshot-6.png" />
    <Img src="/starchild/starchild-gif-1.gif" />
    <Img src="/starchild/starchild-gif-2.gif" />
  {/snippet}
  {#snippet images()}
    <Img src="/starchild/starchild-banner.png" />
    <Svg src={StarChildTransparentLogo} />
    <Img src="/starchild/starchild-transparent-logo.png" />
    <Img src="/starchild/starchild-grayscale-logo.png" />
    <Img src="/starchild/starchild-suit-tileset-x4.png" />
  {/snippet}
</PressKit>
