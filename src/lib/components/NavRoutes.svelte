<script lang="ts">
  import { page } from "$app/stores";

  interface Props {
    routes?: Routes[];
  }

  let { routes = [] }: Props = $props();

  let currentRoute = $derived($page.url.pathname);
</script>

{#each routes as route}
  <a href={route.url} class:font-bold={route.url === currentRoute}
    >{route.label.toUpperCase()}</a
  >
{/each}
