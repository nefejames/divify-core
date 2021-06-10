<script>
  import { Button } from "../components";
  import Illustration from "../illustration.svelte";
</script>

<!-- * * add gsap for logo and image.the image should have a reveal curtain onmount -->
<!-- add light theme toggle -->
<!-- write articles : 1-using emotion in svelte; 2-conditional styling in svelte
3-theme toggling in svelte
-->
<section>
  <div class="hero-left">
    <div class="hero-copy">
      <h2>We are <span>DivifyCore</span></h2>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum sapiente
        distinctio, quaerat deleniti soluta minus consectetur placeat doloribus
        architecto eum.
      </p>
    </div>
    <div class="cta-box">
      <Button buttonCopy="Get Started" isPrimaryBtn />
      <Button buttonCopy="Learn More" />
    </div>
  </div>
  <div class="hero-right illustration-box">
    <Illustration />
  </div>
</section>

<style>
  section {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }

  .hero-left {
    width: auto;
    margin-bottom: 2rem;
  }

  .hero-copy {
    margin-bottom: 2rem;
  }

  .illustration-box {
    height: 450px;
    width: 100%;
  }

  h2 {
    color: var(--text-color);
    font-size: calc(2.3rem + 0.7vw);
    margin-bottom: 1rem;
  }

  p {
    font-size: 1.2rem;
    color: var(--text-color);
  }

  span {
    color: var(--primary-color);
  }

  @media (min-width: 640px) {
    section {
      flex-direction: row;
    }

    .illustration-box {
      width: 560px;
      margin-top: -4rem;
    }

    .hero-left {
      width: 45%;
    }
  }
</style>
