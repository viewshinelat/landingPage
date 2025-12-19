<script>
  let menuOpen = false;
  import { onMount } from "svelte";
  let canScroll = false;
  onMount(() => {
    canScroll = true;
  });
  function scrollToSection(id) {
    if (!canScroll) return;
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: "smooth" });
      menuOpen = false;
    }
  }
</script>

<nav class="navbar navbar-grid">
  <div class="logo">
    <img src="/img/fixlat.svg" alt="Fixlat Logo" />
  </div>
  <button
    class="menu-toggle"
    on:click={() => (menuOpen = !menuOpen)}
    aria-label="Abrir menú"
  >
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
  </button>
  <ul class:open={menuOpen}>
    <li>
      <a href="#hero" on:click|preventDefault={() => scrollToSection("hero")}
        >Inicio</a
      >
    </li>
    <li>
      <a href="#sobre" on:click|preventDefault={() => scrollToSection("sobre")}
        >Sobre</a
      >
    </li>
    <li>
      <a
        href="#beneficios"
        on:click|preventDefault={() => scrollToSection("beneficios")}
        >Beneficios</a
      >
    </li>
    <li>
      <a
        href="#experiencia"
        on:click|preventDefault={() => scrollToSection("experiencia")}
        >Experiencia</a
      >
    </li>
  </ul>
  <a
    href="#"
    on:click={() => scrollToSection("contacto")}
    class="cta-nav align-right">Contacto</a
  >
</nav>

<style>
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: #fff;
    color: #0a2540;
    z-index: 1000;
    box-shadow: 0 2px 16px rgba(44, 62, 80, 0.07);
    border-bottom: 1px solid #eaf1f8;
    transition: box-shadow 0.2s;
    gap: 0;
  }
  .navbar-grid {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    height: 70px;
    width: 100%;
    box-sizing: border-box;
  }
  .logo {
    display: flex;
    align-items: center;
    font-family: "Roboto", Arial, sans-serif;
  }
  .logo img {
    height: 45px;
  }
  .menu-toggle {
    display: none;
    flex-direction: column;
    justify-content: center;
    background: none;
    border: none;
    cursor: pointer;
    height: 40px;
    width: 40px;
  }
  .menu-toggle .bar {
    width: 28px;
    height: 4px;
    background: #fff;
    margin: 4px 0;
    border-radius: 2px;
    transition: 0.3s;
  }
  ul {
    display: flex;
    gap: 12px;
    list-style: none;
    margin: 0 auto;
    padding: 0;
    flex-wrap: nowrap;
    min-width: 0;
    max-width: 900px;
    justify-content: center;
    width: 100%;
  }
  .align-right {
    margin-left: auto;
  }
  ul li a {
    color: #0a2540;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.98rem;
    padding: 6px 8px;
    border-radius: 6px;
    transition:
      background 0.18s,
      color 0.18s;
  }
  ul li a:hover {
    background: #f7f9fb;
    color: #1e90ff;
  }
  .cta-nav {
    background: linear-gradient(90deg, #1e90ff 0%, #0072c6 100%);
    color: #fff !important;
    font-weight: bold;
    border-radius: 8px;
    padding: 8px 18px !important;
    margin-left: 24px;
    margin-right: 0;
    box-shadow: 0 2px 8px rgba(30, 144, 255, 0.1);
    transition:
      background 0.2s,
      color 0.2s,
      transform 0.2s;
    white-space: nowrap;
    font-size: 1rem;
    min-width: 90px;
    text-align: center;
    display: inline-block;
    flex-shrink: 0;
    flex-basis: 110px;
    align-self: center;
  }
  @media (max-width: 1200px) {
    ul {
      font-size: 0.97rem;
      gap: 8px;
    }
    .cta-nav {
      margin-right: 8px;
    }
  }
  .cta-nav:hover {
    background: linear-gradient(90deg, #0072c6 0%, #1e90ff 100%);
    color: #fff !important;
    transform: translateY(-2px) scale(1.04);
  }
  @media (max-width: 900px) {
    .menu-toggle {
      display: flex;
    }
    ul {
      position: absolute;
      top: 70px;
      left: 0;
      width: 100%;
      background: #fff;
      flex-direction: column;
      gap: 0;
      display: none;
      box-shadow: 0 2px 16px rgba(44, 62, 80, 0.07);
      border-bottom: 1px solid #eaf1f8;
    }
    ul.open {
      display: flex;
    }
    ul li {
      border-bottom: 1px solid #eaf1f8;
      text-align: center;
      padding: 18px 0;
    }
    ul li a,
    .cta-nav {
      color: #0a2540 !important;
      background: none !important;
      box-shadow: none !important;
    }
  }
  body {
    scroll-padding-top: 64px;
  }
  :global(body) {
    background: linear-gradient(
        rgba(255, 255, 255, 0.85),
        rgba(255, 255, 255, 0.85)
      ),
      url("/img/fondo.jpeg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    min-height: 100vh;
  }
</style>
