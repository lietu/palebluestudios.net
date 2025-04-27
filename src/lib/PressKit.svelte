<script lang="ts">
  import PBSLogo from '$lib/assets/PBS_-_Logo.svg';
  import Svg from '$lib/Svg.svelte';
  import Img from '$lib/Img.svelte';

  let {
    trailer,
    name,
    description,
    history,
    features,
    release_date,
    pricing,
    platforms,
    contact,
    links,
    screenshots,
    images
  } = $props();
</script>

<section>
  <p><a href="/">&larr; Main website</a></p>
  <h1>Press kit for {@render name()}</h1>
  <article>
    <div class="trailer">
      {@render trailer()}
    </div>

    <h2>{@render name()}</h2>
    {@render description()}

    <hr />

    <h2>History</h2>
    {@render history()}

    <hr />

    <h2>Features</h2>
    {@render features()}

    <hr />

    <h2>Release</h2>
    <p>{@render release_date()}</p>

    <hr />

    <h2>Pricing</h2>
    <p>{@render pricing()}</p>

    <hr />

    <h2>Platforms</h2>
    <p>{@render platforms()}</p>

    <hr />

    <h2>Contact information</h2>
    <p>{@render contact()}</p>

    <hr />

    <h3>Screenshots and GIFs</h3>
    <p>Click to open full quality source file in a new tab.</p>
    <div class="images">
      {@render screenshots()}
    </div>

    <hr />

    <h3>Image assets</h3>
    <p>Click to open full quality source file in a new tab.</p>
    <div class="images">
      {@render images()}
    </div>

    <hr />

    <h3>Links</h3>
    <p>Click to open in a new tab.</p>
    <ul>
      {#each Object.keys(links) as name}
        <li><a href={links[name]} target="_blank">{name}</a></li>
      {/each}
    </ul>
  </article>

  <article>
    <h2>About Pale Blue Studios, LLC</h2>
    <p>A small indie developer and publisher of games, based in the United States of America.</p>

    <h3>Image assets</h3>
    <div class="images">
      <Svg src={PBSLogo} alt="Pale Blue Studios logo SVG" />
      <Img src="/pbs-social-share-1200x628.png" alt="Pale Blue Studios logo PNG" />
    </div>
  </article>
</section>

<style lang="scss">
  h2, h3 {
    margin-top: 2rem;
  }

  hr {
    margin: 4rem;
    padding: 0;
  }

  .trailer :global(iframe) {
    aspect-ratio: 16 / 9;
    width: 100%;
    height: 100%;
  }

  .images {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem;
    align-items: center;
  }
</style>
