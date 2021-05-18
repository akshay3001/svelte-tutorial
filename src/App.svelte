<script>
  let counter = 0;
  const onCounterUpdate = (type = "increment", step = 1) => {
    console.log({ type });
    console.log({ step });
    counter = type === "increment" ? counter + 1 : counter - 1;
  };
  const onMouseOver = (e) => console.log(e);
</script>

<main>
  <h1>Counter: {counter}</h1>
  <button on:click={() => onCounterUpdate("increment", 5)}>+</button>
  <button on:click={() => onCounterUpdate("decrement", 5)}>-</button>
  <hr />
  <button on:mouseover={onMouseOver}>Mouse over me</button>
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
