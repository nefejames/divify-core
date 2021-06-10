<header>
  <h1>DivifyCore</h1>

  <nav>
    <ul>
      <li><a href="#">About Us</a></li>
      <li><a href="#">Our Services</a></li>
      <li><a href="#">Blog</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    padding: 1rem 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1.5rem;
  }

  h1 {
    font-size: 2rem;
    color: #333;
  }

  ul {
    display: flex;
    list-style: none;
    justify-content: space-between;
    width: 400px;
  }

  a {
    text-decoration: none;
    font-size: 1.1rem;
    color: #333;
  }

  a:hover {
    color: #215ee9;
    transition: all 0.4s;
  }

  @media (min-width: 640px) {
    header {
      margin-bottom: 4rem;
    }
  }
</style>
