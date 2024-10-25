<script>
  /** @type {{children?: import('svelte').Snippet}} */
  let { children } = $props();
</script>

<div class="mx-auto w-full max-w-7xl">
  {@render children?.()}
</div>
