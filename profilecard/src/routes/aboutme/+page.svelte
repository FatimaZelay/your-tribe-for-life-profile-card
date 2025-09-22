<script>
    import HomeButton from '$lib/components/HomeButton.svelte';

    export let data;
    const member = data.member.data[0]; // Directus response zit in .data[0]
  </script>
  
      <h1 class="heading-center">{member.name}</h1>
      <p>{member.bio}</p>
  
      {#if member.squads && member.squads.length}
        <div class="squads">
          <h2>Squads</h2>
          <ul>
            {#each member.squads as squad}
              <li>
                <strong>{squad.squad_id.name}</strong>  
                (cohort {squad.squad_id.cohort}, tribe: {squad.squad_id.tribe.name})
              </li>
            {/each}
          </ul>
        </div>
      {/if}
    </div>
  </main>
  
  <style>
    :root {
      background: #F4E3E8;
    }
  
    .about-page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      padding: 2rem;
      gap: 2rem;
    }
  
    .profile img {
      display: block;
      max-width: 80%;
      height: auto;
      margin: 1rem auto;
    }
  
    .heading-center {
      font-size: 2rem;
      font-weight: bold;
      margin-top: 1rem;
      text-align: center;
    }
  
    .profile p {
      font-size: 1.1rem;
      margin-top: 0.5rem;
      text-align: center;
      max-width: 600px;
    }
  
    .squads {
      margin-top: 2rem;
      text-align: center;
      color:#e4aebc
    }
  
    .squads ul {
      list-style: none;
      padding: 0;
      color: #e4aebc;
    }
  
    .squads li {
      margin: 0.5rem 0;
      font-size: 2rem;
    }
  </style>
  
  
  