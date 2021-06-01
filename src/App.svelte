<script>
  import Button from "./Button.svelte";
  import Card1 from "./Card1.svelte";
  import SlotProps from "./SlotProps.svelte";
</script>

<main>
  <!-- <Button on:custom-button={() => alert("clicked!")} /> -->
  <Card1>
    <h3 slot="header">Heading 123</h3>
    <div slot="body">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facere et vel
      porro aliquid illum accusantium rerum officiis commodi quos earum a eaque
      quae placeat aperiam in praesentium, cumque architecto quisquam.
    </div>
    <p slot="footer">footer</p>
  </Card1>
  <hr />
  <Card1>
    <div slot="body">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facere et vel
      porro aliquid illum accusantium rerum officiis commodi quos earum a eaque
      quae placeat aperiam in praesentium, cumque architecto quisquam.
    </div>
  </Card1>

  <hr />

  <SlotProps>
    <h2 slot="userList" let:firstName let:lastName>
      {firstName}
      {lastName}
    </h2>
  </SlotProps>
  <br />
  <SlotProps>
    <h2 slot="userList" let:firstName let:lastName>
      {lastName}
      {firstName}
    </h2>
  </SlotProps>
  <br />
  <SlotProps />
</main>
