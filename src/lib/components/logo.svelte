<script>
  import video from "$lib/assets/logo.webm";
  let time = 0;
  let duration = 20;
  import { onMount } from "svelte";

  let scrollY = 0;

  let scrollHeight = 0;

  onMount(() => {
    // Total scrollable height of the document
    scrollHeight = document.documentElement.scrollHeight;
  });
  $: {
    time = duration * (scrollY / scrollHeight) * 5;
  }
</script>

<svelte:window bind:scrollY />

<div class="video-container">
  <video
    bind:currentTime={time}
    style:scale={time > 0 ? ".97" : "1"}
    bind:duration
    preload="metadata"
    muted
    src={video}
  ></video>
</div>

<style>
  .video-container {
    video {
      height: auto;
      width: 100%;
      transition: 300ms;
      max-height: 100dvh;
    }
    width: fit;
    margin: auto 0;
    position: relative;
  }
</style>
