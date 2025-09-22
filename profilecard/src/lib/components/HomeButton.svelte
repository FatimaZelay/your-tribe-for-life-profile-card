<script>
    import { goto } from "$app/navigation";
  
    export let label = "Home";
    export let type = "button"; // kan ook "submit" zijn
  
    const goHome = () => goto("/");
  </script>
