<script>
  let names = ["John", "Austin", "Maarques"];
  let data = [
    { name: "John", id: 1 },
    { name: "Austin", id: 2 },
    { name: "Marques", id: 3 },
  ];
</script>

<main>
  <ul>
    {#each names as name, index}
      <li>
        {index + 1}
        {name}
      </li>
    {/each}
  </ul>
  <hr />
  <ul>
    {#each data as d (d.id)}
      <li>
        {d.name}
      </li>
    {/each}
  </ul>
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
