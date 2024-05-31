<script lang="ts">
  import { enhance } from '$app/forms';
  import { pageTitle } from '$lib/stores/pageTitle';
  
  pageTitle.set("Scrum Poker - Leader")

  /** @type {import('./$types').ActionData} */
	export let form;
</script>

{#if !form?.success}
  <form method="POST" action="?/newScrumPokerSession" use:enhance>
    <button type="submit">Create New Session</button>
  </form>
{/if}


{#if form?.success}
  <h2>New session created!</h2>
{/if}
