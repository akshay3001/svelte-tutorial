<script>
  import { counter } from "../store/counter-store";

  const increment = () => {
    counter.update((value) => value + 1);
  };
</script>

<button on:click={increment}>+</button>
