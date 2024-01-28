<script lang="ts">
  // @ts-nocheck
  import { PUBLIC_TAG_ID } from "$env/static/public";
  import { onMount } from "svelte";

  onMount(() => {
    window.dataLayer = window.dataLayer || [];
    window.dataLayer.push({
      "gtm.start": new Date().getTime(),
      event: "gtm.js",
    });
    const gtmScript = document.createElement("script");
    gtmScript.src =
      "https://www.googletagmanager.com/gtm.js?id=" + PUBLIC_TAG_ID;
    document.head.append(gtmScript);
  });
</script>

<a href="/">Home</a>

<slot />
