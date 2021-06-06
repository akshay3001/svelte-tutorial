<script>
  import TabA from "./TabA.svelte";
  import TabB from "./TabB.svelte";
  import TabC from "./TabC.svelte";

  let activeTab = TabA;
</script>

<main>
  <button on:click={() => (activeTab = TabA)}>Tab A</button>
  <button on:click={() => (activeTab = TabB)}>Tab B</button>
  <button on:click={() => (activeTab = TabC)}>Tab C</button>
  <hr />
  <svelte:component this={activeTab} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
