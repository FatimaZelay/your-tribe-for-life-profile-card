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
  
      /* button kleur */
      background: linear-gradient(180deg, #D1AABD 0%, #e4aebc 100%);
      border: 1px solid rgba(0,0,0,0.06);
      box-shadow:
        0 6px 16px rgba(0, 0, 0, 0.10),
        inset 0 1px 0 rgba(255, 255, 255, 0.5);
