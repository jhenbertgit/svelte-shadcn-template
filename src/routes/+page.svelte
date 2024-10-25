<script>
  import { toast } from "svelte-sonner";
  import { Button } from "$lib/components/ui/button";
  import { Container } from "$lib";
</script>

<Container
  ><h1 class="font-bold text-2xl text-center mt-7">Welcome to Mugna Svelte</h1>
  <p class="text-center">
    A pre-configured boilerplate with Svelte 5 and Shadcn UI, complete with a
    ready-to-use dark mode toggle.
  </p>
  <div class="flex flex-col items-center mt-7">
    <Button
      on:click={() =>
        toast("Congrats!, you are now using Shadcn UI", {
          description: "Svelte 5 with Shadcn UI",
          action: {
            label: "Close",
            onClick: () => console.log("Close"),
          },
        })}
      >Test Click
    </Button>
  </div>
</Container>
