<script>
  import { setContext } from "svelte";
  import ComponentA from "./ComponentA.svelte";

  const username = "John Doe";
  const user = {
    username: "John Doe",
    lastLoggedIn: "yesterday",
    location: "India",
  };

  // Context API in svelte is very similar to pubsub, where any component can
  // publish using setContext('unique-key', data) method and other components can receive data
  // by subscribing using getContext('set-context-key') method
  // data can be of any type primitive as well as non-primitive

  setContext("username", username);
  setContext("user-details", user);
</script>

<main>
  <p>Username in App.svelte: {username}</p>
  <p>Username in App.svelte: {JSON.stringify(user, null, 2)}</p>
  <ComponentA />
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
