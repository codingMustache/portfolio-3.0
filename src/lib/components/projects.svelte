<script lang="ts">
  import Project from "$lib/components/project.svelte";

  import nola from "$lib/assets/nola.png";
  import pap from "$lib/assets/pap.png";
  import jolly from "$lib/assets/jolly.png";
  import clare from "$lib/assets/clare.png";
  import sf from "$lib/assets/sf.png";

  const projects: {
    title: string;
    description: string;
    image: string;
    link: string | undefined;
  }[] = [
    {
      title: "Nola Devs",
      description:
        "A webapp for developers in Nola. Connecting developers with opportunities and resources. Providing a platform for collaboration and knowledge sharing. Empowering developers to grow and succeed.",
      image: nola,
      link: "https://www.noladevs.org/",
    },
    {
      title: "Pinch A Penny",
      description: "Syncing multiple services like Ecom, CMS, Email, and more",
      image: pap,
      link: "https://www.pinchapenny.com/",
    },
    {
      title: "Return Manager",
      description: "Syncing multiple services like Ecom, CMS, Email, and more",
      image: pap,
      link: "https://www.pinchapenny.com/",
    },
    {
      title: "Clare Tattoos",
      description:
        "My wife wanted a site that can handle her bookings, update easily and provide a seamless experience for her customers. The site was built using SvelteKit, Sanity CMS and TailwindCSS. She fully designed the site and I implemented it. She wanted something reminiscent of a myspace era internet. ",
      image: clare,
      link: "https://www.clare.tattoo",
    },
    {
      title: "Jolly Swap",
      description:
        "A fun little web app for starting a giftswap using email, allowing users to exchange gifts anonymously. I realized there were a ton of sites that can do this but then I would be giving away my email to services that I don't trust. So I built my own. It's a simple and secure way to exchange gifts with friends and family.",
      image: jolly,
      link: "https://www.jolly-swap.com/",
    },
    {
      title: "SalesForce Developer",
      description: "Syncing multiple services like Ecom, CMS, Email, and more",
      image: sf,
      link: undefined,
    },
  ];
</script>

<h2>Projects</h2>
<div class="projects">
  {#each projects as project}
    <div class="project-wrapper">
      <Project data={project} />
    </div>
  {/each}
</div>

<style>
  h2 {
    color: var(--sec);
    font-family: undero;
    font-size: 42pt;
  }
  .projects {
    display: flex;
    overflow-x: scroll;
    height: 400px;
    width: 97dvw;
    padding: 50px 10px;
    scroll-behavior: smooth;
  }

  .project-wrapper {
    flex: 0 0 30vw;

    display: flex;
    justify-content: center;
    align-items: center;
    transition: 300ms;
  }

  /* Optional: Hide scrollbar for better aesthetics */
  .projects::-webkit-scrollbar {
    display: none;
  }
  .projects {
    -ms-overflow-style: none; /* IE and Edge */
    scrollbar-width: none; /* Firefox */
  }
</style>
