<script>
  import { onMount } from "svelte";
  import { gsap, Elastic } from "gsap";

  let mobileNavOpened = false;
  const toggleMobileNav = () => (mobileNavOpened = !mobileNavOpened);

  onMount(() => {
    let tl = gsap.timeline();

    tl.from("li", {
      duration: 0.75,
      x: 300,
      autoAlpha: 0,
      delay: 1.5,
      ease: Elastic.easeOut(1, 1),
      stagger: {
        each: 0.75,
        amount: 0.5,
      },
    });
  });
</script>

<header>
  <h1 class="logo">DivifyCore</h1>

  <nav class:dropdown-opened={mobileNavOpened}>
    <ul class="dropdown-link-container">
      <li><a href="#about">About Us</a></li>
      <li><a href="#services">Our Services</a></li>
      <li><a href="#blog">Blog</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>

    <button
      class="mobile-dropdown-toggle"
      aria-hidden="true"
      on:click={toggleMobileNav}
    >
      Menu
    </button>
  </nav>
</header>

<style>
  header {
    padding: 1rem 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 4rem;
  }

  h1 {
    font-size: 2rem;
    color: var(--primary-color);
  }

  ul {
    display: flex;
    list-style: none;
    justify-content: space-between;
    width: 400px;
    /* overflow: hidden; */
  }

  a {
    text-decoration: none;
    font-size: 1.1rem;
    color: var(--text-color);
  }

  a:hover {
    color: var(--primary-color);
    transition: all 0.4s;
  }
  .mobile-dropdown-toggle {
    display: none;
    position: relative;
  }

  button {
    padding: 0.5rem 1.2rem;
    cursor: pointer;
    border: none;
    border-radius: 8px;
    outline: none;
    font-size: 1.1rem;
    box-shadow: var(--box-shadow);
  }
  @media (max-width: 768px) {
    header {
      margin-bottom: 1.5rem;
    }
    .logo,
    .mobile-dropdown-toggle {
      z-index: 1;
    }

    .mobile-dropdown-toggle {
      display: initial;
    }

    .dropdown-link-container {
      /* first, make our dropdown cover the screen */
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: 100vh;
      width: 100vw;

      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      background: lightblue;
      z-index: 0;
      opacity: 0;
      transform: translateY(-100%);
      transition: transform 0.2s, opacity 0.2s;
    }

    nav.dropdown-opened > .dropdown-link-container {
      opacity: 1;
      transform: translateY(0);
    }

    li:not(:last-child) {
      margin-bottom: 2rem;
    }
  }
</style>
