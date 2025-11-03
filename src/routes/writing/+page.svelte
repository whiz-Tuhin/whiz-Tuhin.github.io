<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import WritingList from "./WritingList.svelte";
  import writing from "./writing.yaml";
</script>

<Seo
  title="Tuhin Khare – Publications"
  description="Research publications in systems for AI, distributed systems, serverless computing, and cloud infrastructure."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Publications</h2>
  <WritingList data={writing.papers} />
</section>
