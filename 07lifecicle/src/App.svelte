<script>
  import Home from './Home.svelte';
  import Example1 from './Example1.svelte';

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
  <li><a href="/" on:click|preventDefault={() => (menu = 2)}>onMount</a></li>
</ul>

{#if menu === 1}
  <Home />
{:else if menu === 2}
  <Example1 />
{:else}
  <h1>Page Not Found</h1>
{/if}
