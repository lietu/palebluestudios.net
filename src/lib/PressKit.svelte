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
    videos,
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

    <h3>Videos</h3>
    <div class="videos">
      {#each Object.keys(videos) as name}
        <div>
          <video id={`player-${name}`} playsinline controls>
            {#each Object.keys(videos[name]) as type }
            <source src={videos[name][type]} type={type} />
            {/each}
          </video>
        </div>

        {#each Object.keys(videos[name]) as type }
          <div>
            <a href={videos[name][type]} target="_blank">Open in new tab ({type.split("/")[1]})</a>
          </div>
        {/each}
      {/each}
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
    <p>I founded Pale Blue Studios because I have always wanted to create video games. It has been my dream ever since I was a small child. In 2022, I realized that it was no longer inviable for a solo developer to create a quality indie title, due to the amount of engines, education, and resources available.</p>
    <p>I began my first game in 2022, while still working my normal job, but after six months, I had saved up enough money to quit and focus full time on my dream project. Six more months of full-time game development, and <a href="https://store.steampowered.com/app/2312780/Toleo/" target="_blank">Toleo</a> was released on July 20th, 2023. I had finally accomplished a dream that I had since childhood. The all-important step of completing a game was done. Success was small, but I was satisfied with the game that I had created.</p>
    <p>After Toleo's release, I was fortunate enough to partner with <a href="https://cocreators.ee" target="_blank">Cocreators</a> to help me produce the next game. This allows me to continue my game development dreams full-time, and provides much needed marketing and business knowledge. The future looks bright, and all of us on the Pale Blue Studios team are determined to release fun and creative video games well into the future.</p>
    <p>Written by Jay Ingle</p>

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

  .videos {
    video {
      max-width: 100%;
    }
  }
</style>
