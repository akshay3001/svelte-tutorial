<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  function dispatcher() {
    dispatch("child-clicked", {
      clicked: true,
    });
  }
</script>

<h2>Child Component</h2>
<button on:click={dispatcher}>Click Me</button>
