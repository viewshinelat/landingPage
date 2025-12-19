<script>
  // Logos y textos de ejemplo, reemplaza por los definitivos cuando los tengas
  let cases = [
    { src: '/img/logos/servimeters.png', alt: 'Aguas de México', desc: 'Caso: Reducción del 15% en pérdidas de agua no contabilizada - Utilidad MX' },
    { src: '/img/tic.png', alt: 'MinTIC Colombia', desc: 'Caso: Reducción del 15% en pérdidas de agua no contabilizada - Utilidad MX' },
    { src: '/img/logos/inelcime.png', alt: 'AGUAS', desc: 'Caso: Reducción del 15% en pérdidas de agua no contabilizada - Utilidad MX' },
    { src: '/img/logos/conagua.png', alt: 'AGUAS DE MEXICO', desc: 'Caso: Reducción del 15% en pérdidas de agua no contabilizada - Utilidad MX' },
    { src: '/img/logos/jac.png', alt: 'Otro', desc: 'Caso: Reducción del 15% en pérdidas de agua no contabilizada - Utilidad MX' }
  ];

  let current = 0;
  let casesToShow = 5;
  let interval;
  let paused = false;

  function nextCase() {
    current = (current + 1) % cases.length;
  }
  function prevCase() {
    current = (current - 1 + cases.length) % cases.length;
  }

  $: visibleCases = Array.from({length: casesToShow}, (_, i) => cases[(current + i) % cases.length]);

  import { onMount, onDestroy } from 'svelte';
  onMount(() => {
    interval = setInterval(() => {
      if (!paused) nextCase();
    }, 3500);
  });
  onDestroy(() => {
    clearInterval(interval);
  });
</script>

<section class="casos-exito" id="casos-exito">
  <h2 class="casos-titulo">Casos de Éxito Destacados</h2>
  <div class="casos-carrusel">
    <button class="carrusel-btn" on:click={() => { paused = true; prevCase(); setTimeout(() => paused = false, 2000); }} aria-label="Anterior">&#60;</button>
    <div class="casos-logos">
      {#each visibleCases as caso}
        <img src={caso.src} alt={caso.alt} class="caso-logo" />
      {/each}
    </div>
    <button class="carrusel-btn" on:click={() => { paused = true; nextCase(); setTimeout(() => paused = false, 2000); }} aria-label="Siguiente">&#62;</button>
  </div>
  <div class="casos-desc">
    {visibleCases[0].desc}
  </div>
</section>

<style>
.casos-exito {
  text-align: center;
  padding: 64px 0 32px 0;
}
.casos-titulo {
  font-size: 2rem;
  font-weight: 800;
  margin-bottom: 32px;
}
.casos-carrusel {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 18px;
  margin-bottom: 18px;
}
.carrusel-btn {
  background: #e6f0fa;
  border: none;
  border-radius: 50%;
  width: 44px;
  height: 44px;
  font-size: 1.6rem;
  color: #0a2540;
  cursor: pointer;
  box-shadow: 0 2px 8px rgba(10,37,64,0.10);
  transition: box-shadow 0.2s, transform 0.2s;
}
.carrusel-btn:hover {
  box-shadow: 0 4px 16px rgba(30,144,255,0.18);
  transform: scale(1.08);
}
.casos-logos {
  display: flex;
  gap: 32px;
  align-items: center;
  justify-content: center;
}
.caso-logo {
  height: 64px;
  max-width: 120px;
  object-fit: contain;
  background: transparent;
  border-radius: 10px;
  margin: 0 8px;
  transition: transform 0.2s;
}
.caso-logo:hover {
  transform: scale(1.08);
}
.casos-desc {
  font-size: 1.1rem;
  color: #0a2540;
  margin-top: 18px;
}
</style>
