<script>
  import NavBar from "$lib/components/NavBar.svelte";
  import { pageTitle } from '$lib/stores/pageTitle';
</script>

<NavBar />

<div class="content-container">
  <div class="header-container">
    <h1>{$pageTitle}</h1>
  </div>
  <div class="content">
    <slot />
  </div>
</div>

<style>
  .content-container {
    flex: 1;
    margin-left: 1vh;
  }

  .header-container {
    background-color: var(--bg-2);
    border-radius: var(--border-radius);
    flex: 1;
    padding: 0.5rem;
  }

  .content {
    margin-top: 1rem;
  }
</style>
