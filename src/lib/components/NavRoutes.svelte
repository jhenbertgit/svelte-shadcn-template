<script lang="ts">
  import { page } from "$app/stores";
  type Routes = {
    label: string;
    url: string;
  };

  export let routes: Routes[] = [];

  $: currentRoute = $page.url.pathname;

  // const isActive = (route: string) => {
  //   return route === currentRoute;
  // };
</script>

{#each routes as route}
  <a href={route.url} class:font-bold={route.url === currentRoute}
    >{route.label.toUpperCase()}</a
  >
{/each}
