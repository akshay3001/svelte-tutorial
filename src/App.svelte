<script>
  import Heading from "./Heading.svelte";

  const name = "Test";
</script>

<main>
  <!-- Component styles are scoped by default in Svelte -->
  <!-- Meaning, styles applied at component will be applied to that component itself -->
  <!-- To make Global styling available make use of :global() -->
  <h2>Hello {name}!</h2>
  <h3>Hello {name}!</h3>
  <Heading />
</main>

<style>
  :global(h3) {
    color: blue;
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h2 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
