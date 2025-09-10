<script lang="ts">
    export let label: string = "About Me";
    export let type: "button" | "submit" = "button";
    export let onClick: (() => void) | null = null;
  </script>
  
  <svelte:head>
    <link
      href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap"
      rel="stylesheet"
    >
  </svelte:head>
  
  <button
    class="about-pill"
    {type}
    aria-label={label}
    on:click={() => onClick && onClick()}
  >
    {label}
  </button>
  <style>
    .about-pill {
      
      padding: 0.6rem 1.8rem;
      border-radius: 9999px;
