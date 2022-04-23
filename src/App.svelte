<script lang="ts">
  let name: string = "world";
</script>

<header>
  <div class="topBar">
    <a href="tel:+32 69 420 666">+32 69 420 666</a>
    <a
      href="mailto: INFO@E-ELEC.BE
    "
      >INFO@E-ELEC.BE
    </a>
  </div>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</header>
<main />

<style lang="scss">
  header {
    height: 70vh;
    background: linear-gradient(-5deg, white 25%, #6bc9ef 25%);
  }

  .topBar {
    background-color: #ef916b;
    color: white;
    display: flex;
    align-items: flex-end;
  }

  .wrapper {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;

    h1 {
      color: #ff3e00;
      text-transform: uppercase;
      font-size: 4em;
      font-weight: 100;
    }

    @media (min-width: 640px) {
      max-width: none;
    }
  }
</style>
