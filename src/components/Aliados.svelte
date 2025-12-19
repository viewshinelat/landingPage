<script>
  // Lista de logos aliados (agrega aquí los logos que subas a /img/logos)
  let logos = [
    { src: '/img/tic.png', alt: 'MinTIC' },
    { src: '/img/pais.png', alt: 'Plataforma PAIS' },
    { src: '/img/logos/inelcime.png', alt: 'INELCIME' },
    { src: '/img/logos/conagua.png', alt: 'CONAGUA' },
    { src: '/img/logos/servimeters.png', alt: 'SERVIMETERS' },
    { src: '/img/logos/jac.png', alt: 'JAC' },
    { src: '/img/logos/emcali.png', alt: 'EMCALI' },
    { src: '/img/logos/acueductobogota.jpg', alt: 'Acueducto de Bogotá' },
    { src: '/img/logos/aws.png', alt: 'Amazon Web Services' },
    { src: '/img/logos/alibabacloud.png', alt: 'Alibaba Cloud' },
    { src: '/img/logos/Metrologica.png', alt: 'Metrológica' },
    { src: '/img/logos/medileser.jpeg', alt: 'Medileser' }
  ];

  let current = 0;
  import { onMount, onDestroy } from 'svelte';
  let logosToShow = 6; // Mostrar 6 logos a la vez

  // Responsivo: menos logos en móvil
  function updateLogosToShow() {
    if (window.innerWidth < 700) {
      logosToShow = 2;
    } else if (window.innerWidth < 1000) {
      logosToShow = 4;
    } else {
      logosToShow = 6;
    }
  }

  onMount(() => {
    updateLogosToShow();
    window.addEventListener('resize', updateLogosToShow);
  });
  onDestroy(() => {
    window.removeEventListener('resize', updateLogosToShow);
  });


  // Variable reactiva para los logos visibles
  $: visibleLogos = Array.from({length: logosToShow}, (_, i) => logos[(current + i) % logos.length]);


  function nextLogo() {
    current = (current + 1) % logos.length;
  }
  function prevLogo() {
    current = (current - 1 + logos.length) % logos.length;
  }

  // Autoplay cada 2 segundos, pausando al interactuar
  let interval;
  let paused = false;
  function startAutoplay() {
    stopAutoplay(); // Evita duplicidad
    interval = setInterval(() => {
      if (!paused) nextLogo();
    }, 2000);
  }
  function stopAutoplay() {
    if (interval) clearInterval(interval);
  }
  onMount(() => {
    startAutoplay();
    updateLogosToShow();
    window.addEventListener('resize', updateLogosToShow);
  });
  onDestroy(() => {
    stopAutoplay();
    window.removeEventListener('resize', updateLogosToShow);
  });
</script>
<section class="aliados" id="aliados">
  <h2 class="aliados-titulo">Aliados</h2>
  <div class="aliados-card">
    <div class="aliados-texto">
      Aliado estratégico en la integración de dispositivos IoT para ciudades inteligentes:
    </div>
    <div class="aliados-carrusel">
      <button class="carrusel-btn moderno" on:click={() => { paused = true; prevLogo(); setTimeout(() => paused = false, 2000); }} aria-label="Anterior">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="12" cy="12" r="12" fill="#e6f0fa"/>
          <path d="M14.5 7L10 12L14.5 17" stroke="#0a2540" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>
      <div class="carrusel-viewport">
        {#each visibleLogos as logo}
            <img src={logo.src} alt={logo.alt} class="aliado-logo" />
        {/each}
      </div>
      <button class="carrusel-btn moderno" on:click={() => { paused = true; nextLogo(); setTimeout(() => paused = false, 2000); }} aria-label="Siguiente">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="12" cy="12" r="12" fill="#e6f0fa"/>
          <path d="M10 7L14.5 12L10 17" stroke="#0a2540" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>
    </div>

  </div>
</section>


<style>
.aliados-titulo {
  font-size: 2rem;
  font-weight: 800;
  color: #0a2540;
  margin-bottom: 32px;
  text-align: center;
}
.aliados {
  background: #f7fbfd;
  color: #0a2540;
  padding: 64px 0 48px 0;
  text-align: center;
}
.aliados-card {
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(10,37,64,0.08);
  padding: 32px 18px 24px 18px;
  min-width: 220px;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: box-shadow 0.3s, transform 0.3s;
}
.aliados-texto {
  font-size: 1.08rem;
  margin-bottom: 18px;
}
.aliados-carrusel {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  margin-top: 12px;
}
.carrusel-btn {
  background: transparent;
  border: none;
  border-radius: 50%;
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  box-shadow: 0 2px 8px rgba(10,37,64,0.10);
  margin: 0 8px;
  transition: box-shadow 0.2s, transform 0.2s;
  z-index: 2;
  position: relative;
}
.carrusel-btn.moderno svg {
  display: block;
}
.carrusel-btn:hover {
  box-shadow: 0 4px 16px rgba(30,144,255,0.18);
  transform: scale(1.08);
}
.carrusel-viewport {
  display: flex;
  gap: 32px;
  align-items: center;
  min-width: 0;
  justify-content: center;
  width: 100%;
}
.aliado-logo {
  height: 90px;
  max-width: 170px;
  object-fit: contain;
  background: transparent;
  border-radius: 10px;
  box-shadow: none;
  margin: 0 8px;
  transition: transform 0.2s;
  flex: 1 1 0;
}
.aliado-logo:hover {
  transform: scale(1.08);
}
</style>
