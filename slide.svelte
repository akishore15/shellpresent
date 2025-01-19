<!-- Slide.svelte -->
<script>
  export let content = "";
</script>

<div class="slide">
  {@html content}
</div>

<style>
  .slide {
    padding: 20px;
    border: 1px solid #ccc;
    margin-bottom: 10px;
  }
</style>
