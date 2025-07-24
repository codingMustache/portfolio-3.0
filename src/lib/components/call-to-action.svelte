<script>
  import {
    GithubBrands,
    LinkedinInBrands,
    BlueskyBrands,
    EnvelopeSolid,
  } from "svelte-awesome-icons";
</script>

<div class="card">
  <div class="icons">
    <a href="/">
      <BlueskyBrands size="20px" />
    </a>
    <a href="/">
      <GithubBrands size="20px" />
    </a>
    <a href="/">
      <LinkedinInBrands size="20px" />
    </a>
    <a href="/">
      <EnvelopeSolid size="20px" />
    </a>
  </div>

  <div class="call-to-action">
    <h1>
      Hello There!
      <br />
      I'm <span> Jorge </span>,
      <br />
      A Full Stack
      <br />
      Developer.
    </h1>
  </div>
</div>

<style>
  .card {
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    border-top: 1px solid var(--sec);
    border-bottom: 1px solid var(--sec);
  }

  .icons {
    a {
      color: var(--sec);
      padding: 10px;
    }
    height: 100%;
    width: fit;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }
  .call-to-action {
    height: 100%;
    padding: 20px 50px;
    border-left: 1px solid var(--sec);
    border-right: 1px solid var(--sec);
  }
  h1 {
    line-height: 1.2;
    text-align: end;
    color: var(--sec);
    
    span {
      font-family: harley;
      font-weight: 800;
      text-shadow: none;
    }
  }
</style>
