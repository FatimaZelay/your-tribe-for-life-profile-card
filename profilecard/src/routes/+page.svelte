<script>
    import AboutMeButton from '$lib/components/AboutMeButton.svelte';

    const goToAbout = () => {
    console.log("Go to about page");
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

  </style>
  