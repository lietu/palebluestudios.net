<script lang="ts">

  import '@fontsource/jersey-15';

  // Import global styles
  import "$styles/init.scss"

  let {children} = $props()
</script>

<svelte:head>
  <!-- Primary Meta Tags -->
  <title>Pale Blue Studios - Indie game studio</title>
  <meta name="title" content="Pale Blue Studios - Indie game studio" />
  <meta name="description" content="We're a small indie game studio. Currently working on Star Child - a pixel art metroidvania game. Our previous game, Toleo is out now on Steam and Itch!" />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://palebluestudios.net/" />
  <meta property="og:title" content="Pale Blue Studios - Indie game studio" />
  <meta property="og:description" content="We're a small indie game studio. Currently working on Star Child - a pixel art metroidvania game. Our previous game, Toleo is out now on Steam and Itch!" />
  <meta property="og:image" content="https://palebluestudios.net/pbs-social-share-1200x628.png" />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:title" content="Pale Blue Studios - Indie game studio" />
  <meta property="twitter:description" content="We're a small indie game studio. Currently working on Star Child - a pixel art metroidvania game. Our previous game, Toleo is out now on Steam and Itch!" />
  <meta property="twitter:image" content="https://palebluestudios.net/pbs-social-share-1200x628.png" />

  <!-- Meta Tags Generated with https://metatags.io -->

  <!-- Plausible analytics, privacy friendly -->
  <!-- https://plausible.io/privacy -->
  <script defer data-domain="palebluestudios.net" src="https://plausible.io/js/script.js"></script>
  <script>window.plausible = window.plausible || function() { (window.plausible.q = window.plausible.q || []).push(arguments) }</script>
</svelte:head>

<main>
  {@render children()}
</main>
<footer>
  <p>Copyright &copy; Pale Blue Studios, LLC 2025</p>
  <p>For business inquiries contact us at <a href="mailto:palebluetx@gmail.com">palebluetx@gmail.com</a></p>
</footer>

<style lang="scss">
  :global(html, body), root {
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  $padding: 1rem;

  main, footer {
    padding: $padding;
    flex-grow: 1;
    max-width: 40rem;
    margin: auto;
  }

  footer {
    text-align: center;
    margin-top: 4rem;
  }
</style>
