<script lang="ts">
  let { src, alt } = $props();
</script>

<div class="img">
  <a href={src} target="_blank" aria-label={alt}><img src={src} alt={alt} /></a>
</div>

<style lang="scss">
  .img {
    width: 100%;
    height: 100%;
    padding: 0.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .img img {
    max-width: 100%;
  }

  .img:hover {
    background-color: rgba(255, 255, 255, 0.025);
  }
</style>
