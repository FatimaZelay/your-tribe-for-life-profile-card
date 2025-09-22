<script>
    import HomeButton from '$lib/components/HomeButton.svelte';

    export let data;
    const member = data.member.data[0]; // Directus response zit in .data[0]
  </script>
