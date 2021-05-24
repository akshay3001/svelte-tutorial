<script>
  import Hello from "./Hello.svelte";
  const user = {
    username: "John Doe",
    lastLoggedIn: "yesterday",
  };
</script>

<main>
  <Hello username="Test User" lastLoggedIn="yesterday" />
  <hr />
  <Hello {...user} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
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
