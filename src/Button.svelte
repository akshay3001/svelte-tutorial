<script>
  import { createEventDispatcher } from "svelte";
  const dispath = createEventDispatcher();

  function onButtonClick() {
    dispath("custom-button");
  }
</script>

<button class="btn" on:click={onButtonClick}>
  <slot name="button-text">Submit</slot>
</button>

<style>
  .btn {
    background-color: lightskyblue;
    padding: 10px;
    font-size: 12px;
  }
</style>
