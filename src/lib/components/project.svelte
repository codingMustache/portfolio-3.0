<script lang="ts">
  export let data: {
    title: string;
    description: string;
    image: string;
    link?: string;
  };

  let flipped = false;

  function toggleFlip() {
    flipped = !flipped;
  }
</script>

<button class="card-wrapper" on:click={toggleFlip}>
  <div class:flipped class="card">
    <!-- Front -->
    <div class="card-face card-front">
      <img src={data.image} alt={data.title} />
      <h2>{data.title}</h2>
    </div>

    <!-- Back -->
    <div class="card-face card-back">
      <p>{data.description}</p>
      {#if data.link}
        <a href={data.link} target="_blank" rel="noopener noreferrer"
          >View Project</a
        >
      {/if}
    </div>
  </div>
</button>

<style>
  button {
    background: none;
    border: none;
  }
  .card-wrapper {
    perspective: 1000px;
    width: 500px;
    height: 400px;
    cursor: pointer;
  }

  .card {
    position: relative;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    transition: transform 0.6s ease;
  }

  .card.flipped {
    transform: rotateY(180deg);
  }

  .card-face {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    border-radius: 3px;
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    background: var(--lg);
  }

  .card-front {
    background-color: #000;
    h2 {
      position: absolute;
      bottom: -45px;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 24px;
      font-weight: bold;
      color: var(--sec);
      text-align: center;
      font-weight: 800;
      text-shadow: 0.5px black;
      border-radius: 40px 40px 0 0;
      width: 90%;
      padding: 10px;
      font-size: 32pt;
      background: rgba(0, 0, 0, 0.4);
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
      text-shadow: 1px 1px 3px black;
      backdrop-filter: blur(15px);
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      filter: blur(3px) grayscale(10%);
      background-color: black;
      transition: 300ms;
    }
  }
  .card-front:hover img {
    filter: blur(0px);
  }

  .card-back {
    background-color: var(--sec);
    color: var(--main);
    transform: rotateY(180deg);
    text-align: start;
    display: flex;
    border-radius: 50px;
    flex-direction: column;
    align-items: start;
    justify-content: space-between;
    padding: 30px 50px;
    box-shadow:
      inset 0px 0px 10px 5px var(--sec),
      inset 0px 0px 10px 10px rgba(255, 255, 255, 0.5),
      inset 0px 0px 10px 15px var(--sec),
      inset 0px 0px 10px 20px rgba(0, 0, 0, 0.5);
  }
  h2 {
    font-size: 32pt;
    font-weight: 100;
    margin-bottom: 10px;
    font-family: lucid;
  }

  a {
    color: var(--main);
    font-weight: bold;
    margin-top: 10px;
    display: inline-block;
    align-self: end;
    justify-self: end;
  }
</style>
