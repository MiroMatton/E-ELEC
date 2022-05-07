<script lang="ts">
  import { fade } from "svelte/transition";
  const option1 = "huizen";
  const option2 = "bedrijven";
  let active = { button1: false, button2: false, button3: false };
  let displayOption1;
  let displayOption2;
  const Sort = (sort) => {
    if (sort === "alles") {
      displayOption1 = "";
      displayOption2 = "";
      active.button2 = false;
      active.button3 = false;
      active.button1 = !active.button1;
    }
    if (sort === option1) {
      displayOption2 = displayOption2 == "none" ? "" : "none";
      displayOption1 = "";
      active.button1 = false;
      active.button3 = false;
      active.button2 = !active.button2;
    } else if (sort === option2) {
      displayOption1 = displayOption1 == "none" ? "" : "none";
      displayOption2 = "";
      active.button1 = false;
      active.button2 = false;
      active.button3 = !active.button3;
    }
  };
</script>

<section id="realisatie">
  <div class="container">
    <h2>realisatie</h2>

    <div class="nav">
      <button class:active={active.button1} id="" on:click={() => Sort("alles")}
        >alles</button
      >
      <button class:active={active.button2} on:click={() => Sort(option1)}
        >huizen</button
      >
      <button class:active={active.button3} on:click={() => Sort(option2)}
        >bedrijven</button
      >
    </div>
  </div>
  <div class="grid">
    <div id="Gent" class={displayOption1}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Gent" class={displayOption1}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div transition:fade id="Gent" class={displayOption1}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Kortrijk" class={displayOption1}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Gent" class={displayOption2}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Kortrijk" class={displayOption2}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Kortrijk" class={displayOption2}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
    <div id="Kortrijk" class={displayOption2}>
      <h3 class="underline white">Kortrijk</h3>
    </div>
  </div>
</section>

<style lang="scss">
  @use "../styles/global";

  #realisatie {
    h2 {
      font-size: 2rem;
      text-transform: uppercase;
    }
    background-color: global.$blue;
    color: white;
    padding: 3em;
  }

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
  }

  button {
    background: white;
    color: global.$blue;
    padding: 0.5em 1rem;
    margin: 1em 0 1em 1em;
    font-size: 1.5rem;

    &:hover {
      background-color: global.$orange;
      color: white;
    }
  }

  .active {
    background-color: global.$orange;
    color: white;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
    grid-gap: 2.5em;

    div {
      position: relative;
      text-align: center;
      background: white;

      &::before {
        content: "";
        display: block;
        height: 0;
        width: 0;
        padding-top: 100%;
      }

      h3 {
        color: white;
        margin: 0;
        position: absolute;
        top: 50%;
        left: 50%;
        margin-right: -50%;
        transform: translate(-50%, -50%);
        opacity: 0;
      }
    }

    @mixin imageHover {
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;

      &:hover,
      &:active {
        background: global.$orange;
        h3 {
          opacity: 1;
        }
      }

      &.none {
        display: none;
        transition: visibility 0s, opacity 0.5s linear;
      }
    }

    #Gent {
      background: url("../../public/assets/gent_licht.jpg");
      @include imageHover;
    }

    #Kortrijk {
      background: url("../../public/assets/Kortrijk_licht.jpg");
      @include imageHover;
    }
  }
</style>
