<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";

  const featuredProjects = [
    {
      name: "MapReduce Framework",
      href: "/projects#mapreduce",
      desc: "distributed master-worker topology with fault tolerance",
    },
    {
      name: "Heterogeneity-aware LLM Router",
      href: "/projects#llm-routing",
      desc: "ILP-guided scheduling for mixed GPU fleets",
      aside: "30% P99 latency reduction",
    },
    {
      name: "AutoDNN Early-Exit Integration",
      href: "/projects#autodnn",
      desc: "adaptive branching policies for inference serving",
    },
  ];
</script>

<Seo
  title="Tuhin Khare"
  description="Graduate student in Computer Science at Georgia Tech specializing in systems for AI, distributed systems, and cloud infrastructure."
/>

<p
  class="layout-md text-black text-xl leading-tight font-light mb-16"
  id="tuhin-is"
>
  <span class="g">is a</span> systems researcher<span class="g">,</span><br />
  engineer<span class="g">, and</span><br />
  builder<span class="g">.</span>
</p>

<div class="layout-md text-lg space-y-14">
  <div class="space-y-5">
    <p>
      I'm a graduate student in Computer Science at
      <a class="link" href="https://www.gatech.edu/">Georgia Tech</a>, advised
      by
      <a class="link" href="https://faculty.cc.gatech.edu/~atumanov/"
        >Prof. Alexey Tumanov</a
      >
      in the Systems for AI Lab.
    </p>

    <p>
      I build production systems that balance <em>performance</em>,
      <em>reliability</em>, and research rigor across inference, serverless, and
      hybrid cloud workloads.
    </p>

    <p>
      Most recently I interned with <a
        class="link"
        href="https://aws.amazon.com/dynamodb/">AWS DynamoDB</a
      >, where I designed leadership failover tooling for JournalDB. Earlier, I
      led cross-cloud orchestration efforts at the
      <a class="link" href="https://dsl.cds.iisc.ac.in/"
        >Distributed Systems Lab, IISc</a
      >.
    </p>
  </div>

  <div class="leading-snug space-y-4">
    <p class="pb-2">Recent projects:</p>

    {#each featuredProjects as project}
      <a class="project-pair" href={project.href}>
        <div class="text-black font-medium">
          {project.name}
          <ArrowUpRight size={18} class="inline text-neutral-400" />
        </div>
        <div>
          <p>{project.desc}</p>
          {#if project.aside}
            <aside>{project.aside}</aside>
          {/if}
        </div>
      </a>
    {/each}
  </div>

  <div class="space-y-5">
    <p>
      My research focuses on <em>systems for AI</em>, with an emphasis on
      programmable inference serving, distributed scheduling, and cloud-native
      control planes. I draw from compiler design, large-scale observability,
      and hardware-aware optimization to build dependable platforms for emerging
      AI workloads.
    </p>

    <p>
      At the Systems for AI Lab, I'm designing policy-decoupled C++ abstractions
      for programmable inference serving that separate deployment topology from
      scheduling logic—delivering 12% accuracy gains, 99.99% SLO attainment, and
      20K QPS throughput on heterogeneous clusters.
    </p>

    <p>
      I previously shipped <em>XFaaS</em>, a cross-cloud orchestration platform
      that delivered 75% latency reductions and 57% cost savings through
      adaptive placement with telemetry-informed routing, collaborating with
      industry partners to operationalize hybrid quantum-classical workflows.
    </p>
  </div>

  <div class="space-y-5">
    <p>
      I'm also the Head TA for ECE 4150 — Cloud Computing at Georgia Tech
      (Spring 2025), leading course delivery, AWS labs, and mentoring
      cloud-native capstones.
    </p>

    <p>
      You can find me on <a
        class="link"
        href="https://www.linkedin.com/in/tuhin-khare/">LinkedIn</a
      >,
      <a class="link" href="https://github.com/whiz-Tuhin">GitHub</a>, or
      <a
        class="link"
        href="https://scholar.google.com/citations?user=gOqbVdUAAAAJ&hl=en"
        >Google Scholar</a
      >. Feel free to reach out at
      <a class="link" href="mailto:tkhare7@gatech.edu">tkhare7@gatech.edu</a>.
    </p>
  </div>

  <div class="space-y-5">
    <img
      alt="Tuhin Khare portrait"
      src="https://avatars.githubusercontent.com/u/43981969?v=4"
    />
  </div>
</div>

<style lang="postcss">
  .g {
    @apply text-neutral-400;
  }

  em {
    @apply font-serif text-[110%] leading-[100%];
  }

  .project-pair {
    @apply grid sm:grid-cols-[1fr,2fr] gap-y-1 -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors;
  }

  aside {
    @apply mt-0.5 text-base text-neutral-500;
  }

  /* Correction for vertical navigation links on mobile. */
  @media (max-width: 420px) {
    #tuhin-is {
      @apply -mt-10;
    }
  }
</style>
