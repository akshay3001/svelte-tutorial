<script>
  let loginForm = {
    username: "",
    password: "",
    rememberMe: false,
    skills: [],
    domain: "",
  };

  let skills = ["HTML5", "CSS3", "Javascript"];

  const onLogin = (e) => {
    console.log("Login: ", e);
    console.log("Login Form: ", loginForm);
  };
</script>

<main>
  <form on:submit|preventDefault={onLogin}>
    <label for="username">Username</label>
    <input
      type="text"
      id="username"
      name="username"
      bind:value={loginForm.username}
    />
    <label for="password">Password</label>
    <input
      type="password"
      id="password"
      name="password"
      bind:value={loginForm.password}
    />
    <div>
      <label for="remember">Remember me?</label>
      <input
        type="checkbox"
        id="remember"
        name="remember"
        bind:checked={loginForm.rememberMe}
      />
    </div>
    <div>
      {#each skills as skill}
        <input
          type="checkbox"
          id={skill}
          name={skill}
          value={skill}
          bind:group={loginForm.skills}
        />
        <label for={skill}>{skill}</label>
      {/each}
    </div>
    <div>
      <input
        type="radio"
        id="banking"
        name="banking"
        value="banking"
        bind:group={loginForm.domain}
      />
      <label for="banking">Banking</label>
      <input
        type="radio"
        id="agriculture"
        name="agriculture"
        value="agriculture"
        bind:group={loginForm.domain}
      />
      <label for="agriculture">Agriculture</label>
      <input
        type="radio"
        id="extc"
        name="extc"
        value="extc"
        bind:group={loginForm.domain}
      />
      <label for="banking">EXTC</label>
    </div>
    <button type="submit">Login</button>
  </form>

  <hr />
  <pre>
    {JSON.stringify(loginForm, null, 2)}
  </pre>
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
