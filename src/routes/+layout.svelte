<nav>
  <a href="/">Home</a>
  <a href="/estimations/Leader">Story Point Estimations: Leader</a>
  <a href="/estimations/member">Story Point Estimations: Member</a>
</nav>

<div class="content-container">
  <div class="header-container">
    <h1>Header</h1>
  </div>
  <div class="content">
    <slot />
  </div>
</div>

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
