<!-- Editor.svelte -->
<script>
  import { QuillEditor } from 'svelte-quill';
  export let content = "";
  const handleContentChange = (event) => {
      content = event.target.innerHTML;
  };
</script>

<QuillEditor
  bind:this={editor}
  on:input={handleContentChange}
/>
<style>
  .editor {
    border: 1px solid #ccc;
    min-height: 100px;
  }
</style>
