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
  
  <button
    class="about-pill"
    {type}
    aria-label={label}
    on:click={goHome}
  >
    {label}
  </button>
  
  <style>
    .about-pill {
      padding: 0.6rem 1.8rem;
      border-radius: 9999px;
      background: linear-gradient(180deg, #D1AABD 0%, #e4aebc 100%);
      border: 1px solid rgba(0,0,0,0.06);
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.10), inset 0 1px 0 rgba(255, 255, 255, 0.5);
      font-family: "Great Vibes", ui-serif, Georgia, "Times New Roman", serif;
      font-size: clamp(1.35rem, 2.2vw, 2rem);
      line-height: 1;
      color: #312c2c;
      letter-spacing: 0.02em;
  
      cursor: url('/cursor.png') 0 0, auto;
      transition: transform 140ms ease, box-shadow 140ms ease, filter 140ms ease;
      -webkit-tap-highlight-color: transparent;
    }
  
    .about-pill:active {
      transform: translateY(0);
      box-shadow:
        0 4px 10px rgba(0,0,0,0.10),
        inset 0 2px 4px rgba(0,0,0,0.08);
    }
  </style>
  