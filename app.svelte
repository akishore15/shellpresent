<!-- App.svelte -->
<script>
  import { onMount } from "svelte";
  import Slide from "./Slide.svelte";

  let slides = [];

  onMount(async () => {
      const response = await fetch("http://localhost:8080/api/slides");
      slides = await response.json();
  });
</script>

{#each slides as slide}
  <Slide content={slide}/>
{/each}
