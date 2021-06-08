<script>
  import { counter } from "../store/counter-store";

  function reset() {
    counter.set(0);
  }
</script>

<button on:click={reset}>Reset</button>
