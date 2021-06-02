<script>
  import { onMount } from "svelte";
  const usersUrl = "https://jsonplaceholder.typicode.com/users";
  let users = [];

  onMount(async () => {
    const usersResponse = await fetch(usersUrl);
    users = await usersResponse.json();
    return users;
  });
</script>

{#if users.length}
  <table border="1">
    <thead>
      <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Username</th>
        <th>Email</th>
        <th>Phone Number</th>
        <th>Company Name</th>
      </tr>
    </thead>
    <tbody>
      {#each users as user (user.id)}
        <tr>
          <td>{user.id}</td>
          <td>{user.name}</td>
          <td>{user.username}</td>
          <td>{user.email}</td>
          <td>{user.phone}</td>
          <td>{user.company.name}</td>
        </tr>
      {/each}
    </tbody>
  </table>
{:else}
  Loading Users
{/if}

<style>
  th,
  td {
    padding: 10px;
  }
</style>
