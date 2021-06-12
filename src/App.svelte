<script>
  import Layout from "./Layout.svelte";
  import { Header } from "./components";
  import { Hero } from "./sections";

  // two more things:
  //1.add dark mode
  //2.add gsap animations,maybe even to the navbar on mobile also
</script>

<Layout>
  <Header />
  <Hero />
</Layout>

<style>
  @media (min-width: 640px) {
  }
</style>
