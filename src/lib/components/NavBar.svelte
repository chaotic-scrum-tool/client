<script>
  import Accordion from "$lib/components/Accordion.svelte";
</script>

<nav>
  <a href="/">Home</a>
  <Accordion class="navbar-accordion">
    <!-- svelte-ignore a11y-missing-attribute -->
    <!-- Using <a> to match styling -->
    <a slot="header">Scrum Poker</a>
    <div slot="content">
      <a href="/estimations/leader">Leader</a>
      <a href="/estimations/member">Member</a>
    </div>
  </Accordion>
</nav>

<style>
  nav {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    width: 17vw;
    gap: 1rem;
    padding: 1rem;
    background: var(--bg-2);
    border-radius: var(--border-radius);
  }

  nav a {
    font-weight: 500;
    text-decoration: none;
  }

  :global(.navbar-accordion) {
		cursor: pointer;
		display: inherit;
    flex-direction: inherit;
    gap: 0.5rem;
	}

  :global(div.header a:active) {
		display: flex;
		justify-content: space-between;
		color: inherit;
	}

  :global(.navbar-accordion .content) {
    margin-left: 0.3rem;
  }

  :global(.navbar-accordion .content a) {
		display: inherit;
    margin-bottom: 0.5rem;
  }
</style>
