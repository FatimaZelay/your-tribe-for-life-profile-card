<script>
    import { goto } from "$app/navigation";
  
    export let label = "Home";
    export let type = "button"; // kan ook "submit" zijn
  
    const goHome = () => goto("/");
  </script>
  

<svelte:head>
    <link
      href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap"
      rel="stylesheet"
    >
  </svelte:head>
