<script>
  import me from "$lib/assets/avatar.webp";
</script>

<div class="card">
  <div class="me">
    <img src={me} alt="me smiling" />
    <h3>@Jorge</h3>
  </div>
  <p>
    I'm constantly building, learning and gardening. I have a homelab and I can
    talk your ear off about it if you let me. If you're here and you have made
    it this far,
    <a aria-label="email me" href="mailto:hello@codingMustache.dev">
      email me
    </a>. I would love to build something with or for you or just a chat.
  </p>
</div>

<style>
  .card {
    margin: 100px auto;
    max-width: 500px;
    border-radius: 70px;
    box-shadow:
      inset 0px 0px 10px 5px var(--sec),
      inset 0px 0px 10px 10px rgba(255, 255, 255, 0.5),
      inset 0px 0px 10px 15px var(--sec),
      inset 0px 0px 10px 20px rgba(0, 0, 0, 0.5);
    padding: 10px;
    background-color: var(--sec);
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 50px 100px;
    color: var(--dp);
    p {
      line-height: 1.5;
    }
    .me {
      display: flex;
      align-items: center;
      justify-content: start;
      gap: 5px;
      h3 {
        font-family: roboto;
        font-weight: 600;
        font-size: 22pt;
      }
      img {
        height: 50px;
        width: 50px;
        border-radius: 100%;
      }
    }
  }
  a {
    color: var(--dp);
    text-decoration: none;
    font-weight: 600;
  }
</style>
