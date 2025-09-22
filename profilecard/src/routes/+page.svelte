<script>
    import AboutMeButton from '$lib/components/AboutMeButton.svelte';
    import { goto } from '$app/navigation';
  
    const goToAbout = () => {
      goto('/aboutme');   // dit navigeert naar aboutme pagina
    };
  </script>
  
  <main class="page">
    <!-- Button -->
    <AboutMeButton onClick={goToAbout} />
  
    <div class="camera-wrapper">
      <img src="/digitalcamera.png" alt="Camera" class="camera" />
    </div>
  </main>
  
  <style>
    .page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      padding: 2rem;
      background: #F4E3E8;
      gap: 2rem;
    }
    
    .camera {
      display: block;
      max-width: 80%;
      height: auto;
      margin: 1rem auto;
    }
  </style>
  
  