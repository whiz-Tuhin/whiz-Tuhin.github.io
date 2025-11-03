<script lang="ts">
  export let title: string;
  export let ogTitle: string | null = null;
  export let description: string;
</script>

<svelte:head>
  <title>{title}</title>
  <meta name="description" content={description} />
  <meta property="og:title" content={ogTitle ?? title} />
  <meta property="og:description" content={description} />
  <meta
    property="og:image"
    content="https://avatars.githubusercontent.com/u/43981969?v=4"
  />
  <meta name="twitter:card" content="summary" />
</svelte:head>
