<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Tuhin Khare – Resume"
  description="Graduate student in Computer Science at Georgia Tech specializing in systems for AI, distributed systems, and cloud infrastructure."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Professional Work</h2>

  <Workplace
    title="Software Development Engineering Intern"
    company="AWS DynamoDB"
    url="https://aws.amazon.com/dynamodb/"
    dates="May 2025 – Aug 2025"
    location="Seattle, WA"
    logo="/images/aws.svg"
  >
    <li>
      Built one-command tooling to orchestrate JournalDB leadership failover,
      automating secondary promotion, quorum reconfiguration, and health
      validation across shards.
    </li>
    <li>
      Achieved sub-second recovery while preserving change-control guardrails
      across multi-region fleets.
    </li>
  </Workplace>

  <Workplace
    title="Graduate Researcher"
    company="Systems for AI Lab, Georgia Tech"
    url="https://faculty.cc.gatech.edu/~atumanov/"
    dates="Aug 2024 – Present"
    location="Atlanta, GA"
    logo="/images/GTVertical_RGB.svg"
  >
    <li>
      Designing policy-decoupled C++ abstractions for programmable inference
      serving that separate deployment topology from scheduling logic.
    </li>
    <li>
      The resulting runtime delivers 12% accuracy gains, 99.99% SLO attainment,
      and 20K QPS throughput on heterogeneous clusters.
    </li>
  </Workplace>

  <Workplace
    title="Senior Research Engineer"
    company="Distributed Systems Lab, IISc"
    url="https://dsl.cds.iisc.ac.in/"
    dates="Aug 2020 – May 2024"
    location="Bengaluru, India"
    logo="/images/iisc.svg"
  >
    <li>
      Led XFaaS, a cross-cloud orchestration platform that delivered 75% latency
      reductions and 57% cost savings by pairing adaptive placement with
      telemetry-informed routing.
    </li>
    <li>
      Collaborated with industry partners to operationalize hybrid
      quantum-classical workflows, with research featured in IEEE/ACM CCGrid
      2023 and 2025.
    </li>
    <li>
      Contributed to Triparts, a scalable streaming graph partitioning system
      (accepted to VLDB 2025).
    </li>
  </Workplace>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Education</h2>

  <div class="mb-6">
    <div class="flex items-start gap-3 mb-2">
      <img
        src="/images/GTVertical_RGB.svg"
        alt="Georgia Tech logo"
        class="w-20 h-20 object-contain flex-shrink-0 mt-0"
      />
      <div class="flex-1">
        <div class="flex justify-between items-end">
          <h3 class="text-black text-lg">Georgia Institute of Technology</h3>
          <div class="text-neutral-500 mb-0.5">2024 — Present</div>
        </div>
        <p class="byline">M.S. in Computer Science</p>
        <p class="mt-2">Specialization: Systems for AI</p>
        <p>Advisor: Prof. Alexey Tumanov</p>
      </div>
    </div>
  </div>

  <div class="mb-6">
    <div class="flex items-start gap-3 mb-2">
      <img
        src="/images/manipal-vertical.png"
        alt="Manipal logo"
        class="w-20 h-20 object-contain flex-shrink-0 mt-0"
      />
      <div class="flex-1">
        <div class="flex justify-between items-end">
          <h3 class="text-black text-lg">Manipal Institute of Technology</h3>
          <div class="text-neutral-500 mb-0.5">2016 — 2020</div>
        </div>
        <p class="byline">B.Tech. in Computer Science</p>
      </div>
    </div>
  </div>

  <h4 class="font-medium mt-4 mb-1">Teaching:</h4>
  <ul>
    <li>
      Head Teaching Assistant for ECE 4150 — Cloud Computing, Georgia Tech
      (Spring 2025)
    </li>
    <li>
      Led course delivery, AWS labs, and mentor program for cloud-native
      capstones
    </li>
  </ul>

  <h4 class="font-medium mt-4 mb-1">Graduate coursework:</h4>
  <ul>
    <li>Advanced Operating Systems (CS 6210)</li>
    <li>High Performance Computer Architecture (CS 6290)</li>
    <li>Graduate Algorithms (CS 6515)</li>
    <li>Distributed Systems (CS 6421)</li>
  </ul>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Publications</h2>

  <div class="mb-4">
    <ul>
      <li>
        <b
          >QuArch: A Benchmark for Evaluating LLM Reasoning in Computer
          Architecture.</b
        >
        <em>ICLR</em>, 2026 (submitted).
      </li>
      <li>
        <b
          >Triparts: Scalable Streaming Graph Partitioning to Enhance Community
          Structure.</b
        >
        <em>VLDB</em>, 2025 (accepted).
      </li>
      <li>
        <b
          >Choreography and Profiling of Quantum-Classical FaaS Workflows on
          Hybrid Clouds.</b
        >
        <em>IEEE/ACM CCGrid</em>, 2025.
      </li>
      <li>
        <b
          >XFaaS: Cross-platform Orchestration of FaaS Workflows on Hybrid
          Clouds.</b
        >
        <em>IEEE/ACM CCGrid</em>, 2023.
      </li>
    </ul>
  </div>

  <p class="mt-4">
    Full list available on
    <a
      class="link"
      href="https://scholar.google.com/citations?user=gOqbVdUAAAAJ&hl=en"
      >Google Scholar</a
    >.
  </p>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Service</h2>

  <ul>
    <li>Reviewer for <em>VLDB 2025</em>, <em>SoCC 2024</em></li>
    <li>Mentor for <em>Women in Computing @ GT</em> systems reading group</li>
    <li>Organizer for Systems for AI Lab hack nights</li>
  </ul>
</section>

<style lang="postcss">
  b {
    @apply font-medium;
  }

  ul {
    @apply list-disc pl-7 marker:text-neutral-400;
  }

  .byline {
    @apply font-serif italic;
  }
</style>
