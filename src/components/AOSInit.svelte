<script>
  import { onMount } from 'svelte';
  import AOS from 'aos';
  onMount(() => {
    AOS.init({ once: true });
  });
</script>
