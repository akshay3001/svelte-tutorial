<script>
</script>

<section class="card">
  <header class="card__header">
    <slot name="header">
      <h3>Default Heading</h3>
    </slot>
  </header>
  <div class="card__body">
    <slot name="body" />
  </div>
  {#if $$slots.footer}
    <hr />
  {/if}
  <footer class="card__footer" name="footer">
    <slot name="footer">Default Footer</slot>
  </footer>
</section>

<style>
  .card {
    max-height: 300px;
    max-width: 300px;
    border-radius: 8px;
    padding: 10px;
    box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.75);
    -webkit-box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.75);
  }
  .card__body {
    font-size: 1rem;
  }
  .card__footer {
    padding-top: 20px;
    font-size: 10px;
  }
</style>
