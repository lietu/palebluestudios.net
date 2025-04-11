<script lang="ts">
  let { src } = $props();
  let container: HTMLElement

  function open(evt) {
    evt.preventDefault()
    evt.stopPropagation()

    const svg = container.querySelector("svg")
    const svg_as_string = new XMLSerializer().serializeToString(svg)
    const blob = new Blob([svg_as_string], {type: "image/svg+xml"})
    const url = URL.createObjectURL(blob)
    const win = window.open(url)
    win.onload = (evt) => URL.revokeObjectURL(url)
  }
</script>

<div class="svg" bind:this={container}>
  <a href="#" onclick={open} title="Open SVG in new tab">{@render src({})}</a>
</div>

<style lang="scss">
  .svg {
    width: 100%;
    height: 100%;
    padding: 0.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .svg:hover {
    background-color: rgba(255, 255, 255, 0.025);
  }

  .svg :global(svg) {
    max-width: 100%;
  }

  a, a:active, a:hover, a:visited {
    color: unset;
  }

</style>
