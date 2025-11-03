<script lang="ts">
  import { page } from "$app/stores";

  import { onMount } from "svelte";

  import Seo from "$lib/components/Seo.svelte";
  import Project from "./Project.svelte";

  const projects = import.meta.glob("../../projects/*.md", {
    eager: true,
  }) as any;
  const images = import.meta.glob("../../projects/*.{png,jpg,svg}", {
    eager: true,
  }) as any;

  function trimName(id: string) {
    return id.match(/\.\.\/projects\/(.*)\.md$/)?.[1];
  }

  $: projectsByDate = Object.keys(projects).sort(
    (a, b) => projects[b].date - projects[a].date
  );
  $: projectsByTitle = Object.keys(projects).sort((a, b) => {
    const titleA = projects[a].title.toLowerCase();
    const titleB = projects[b].title.toLowerCase();
    return titleA < titleB ? -1 : titleA > titleB ? 1 : 0;
  });

  onMount(() => {
    // Hack: Fix the scroll position after the page loads, especially for mobile browsers.
    const selected = $page.url.hash.slice(1);
    if (selected) {
      setTimeout(() => {
        if ($page.url.hash.slice(1) === selected) {
          document.getElementById(selected)?.scrollIntoView();
        }
      }, 500);
    }
  });

  let stars: Record<string, number> | null = null;
</script>

<Seo
  title="Tuhin Khare – Projects"
  description="Systems research and engineering projects in distributed systems, AI infrastructure, serverless computing, and cloud-native platforms."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Research & Projects</h2>

  <p class="text-lg mb-4">
    My work spans <em class="font-serif text-[110%] leading-[100%]">systems for AI</em>,
    distributed systems, and cloud infrastructure. I focus on building production-grade
    systems that balance performance, reliability, and research rigor.
  </p>

  <p class="text-lg mb-4">
    These projects range from research prototypes published in top venues to
    production systems handling real workloads at scale.
  </p>

  <p class="text-lg">
    If you'd like to discuss any of these projects,
    <a class="link" href="mailto:tkhare7@gatech.edu?subject=Projects">reach out</a>!
  </p>
</section>

<div class="bg-gray-900 text-neutral-200 dark">
  <section class="layout-md py-12">
    <h2 class="heading2 text-white">Table of Contents</h2>
    <ul class="sm:columns-2">
      {#each projectsByTitle as id (id)}
        <li>
          <a class="link" href="#{trimName(id)}">{projects[id].title}</a>
        </li>
      {/each}
    </ul>
  </section>
</div>

{#each projectsByDate as id (id)}
  <section class="py-10" id={trimName(id)}>
    <div class="mx-auto max-w-[1152px] px-4 sm:px-6">
      <Project data={projects[id]} {images} {stars} />
    </div>
  </section>
{/each}

