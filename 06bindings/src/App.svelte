<script>
  import Home from './Home.svelte';
  import CheckboxInputs from './CheckboxInputs.svelte';
  import NumericInputs from './NumericInputs.svelte';

  export let menu = 1;
</script>

<style>
  ul#menu li {
    display: inline;
  }
</style>

<ul id="menu">
  <li><a href="/" on:click|preventDefault={() => (menu = 1)}>Home</a></li>
  |
  <li><a href="/" on:click|preventDefault={() => (menu = 2)}>Checkbox Inputs</a></li>
  |
  <li><a href="/" on:click|preventDefault={() => (menu = 3)}>Numeric Inputs</a></li>
</ul>

{#if menu === 1}
  <Home />
{:else if menu === 2}
  <CheckboxInputs />
{:else if menu === 3}
  <NumericInputs />
{:else}
  <h1>Page Not Found</h1>
{/if}
