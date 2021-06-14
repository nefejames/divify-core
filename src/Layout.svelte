<main>
  <slot />
</main>

<style>
  :global(:root) {
    --text-color: #333;
    --btn-color: #0d0c22;
    --primary-color: #215ee9;
    --secondary-color: #ea4c89;
    --box-shadow: "0px 0px 0px 1px #e7e7e9 inset";
  }

  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    overflow: hidden;
    /* background: #ebf1ff; */
    /* font-family: Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans",
      "Helvetica Neue", sans-serif; */

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
