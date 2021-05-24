<script>
  import { getContext } from "svelte";

  let username = getContext("username");
  let userDetails = getContext("user-details");
</script>

<h2>Component C</h2>
<strong>Username from ComponentA: {username}</strong>
<br />
<strong
  >User Details from ComponentA: {JSON.stringify(userDetails, null, 2)}</strong
>
