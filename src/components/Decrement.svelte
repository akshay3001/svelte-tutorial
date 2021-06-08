<script>
  import { counter } from "../store/counter-store";

  function decrement() {
    counter.update((value) => value - 1);
  }
</script>

<button on:click={decrement}>-</button>
