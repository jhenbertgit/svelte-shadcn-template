<script lang="ts">
  import { page } from "$app/stores";
  type Routes = {
    label: string;
    url: string;
  };

  export let routes: Routes[] = [];

  $: currentRoute = $page.url.pathname;

  const isActive = (route: string) => {
    return route === currentRoute;
  };
</script>

{#each routes as route}
  <a
    data-sveltekit-reload
    href={route.url}
    class={isActive(route.url) ? "font-bold" : ""}
    >{route.label.toUpperCase()}</a
  >
{/each}
