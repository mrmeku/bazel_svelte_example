<script lang="ts">
  export let name: string = "stranger";
  $: boring = name === "world";
</script>

<div>
  I am a component, sup <span class:boring>{name || "..."}</span>?

  <br />
  {#if boring}
    How unoriginal...
  {:else if !name}
    No name eh?
  {/if}
</div>

<style>
  .boring {
    font-weight: 600;
  }
</style>
