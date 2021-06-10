<main>
  <slot />
</main>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    background: #ebf1ff;
    /* background: #e5e5e5; */
    font-size: 62.5%;
  }

  main {
    height: 100vh;
    padding: 1rem;
  }

  :global(p) {
    line-height: 1.7;
  }

  @media (min-width: 640px) {
    main {
      padding: 1rem 5rem;
    }
  }
</style>
