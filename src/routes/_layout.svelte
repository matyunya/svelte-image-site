<script>
  import { stores } from "@sapper/app";
  import { onMount } from "svelte";
  const { preloading, page } = stores();

  import { fade } from "svelte/transition";

  import Tabs from "components/Tabs";
  import Button from "components/Button";
  import ProgressLinear from "components/ProgressLinear";

  let innerWidth = 0;
</script>

<svelte:head>
  <title>Svelte Image: Responsive optimized images for Svelte</title>
</svelte:head>

{#if $preloading}
  <ProgressLinear app />
{/if}

<main
  class="max-w-3xl mx-auto mb-10 mt-24"
  transition:fade={{ duration: 500 }}>
  <slot />
</main>
