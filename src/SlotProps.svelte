<script>
  const users = [
    {
      firstName: "John",
      lastName: "Doe",
    },
    {
      firstName: "Test",
      lastName: "Testing",
    },
    {
      firstName: "Bruce",
      lastName: "Wayne",
    },
  ];
</script>

{#each users as user (user)}
  <slot name="userList" firstName={user.firstName} lastName={user.lastName}>
    <h3>
      {user.firstName}
      {user.lastName}
    </h3>
  </slot>
{/each}
