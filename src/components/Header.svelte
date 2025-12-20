<header class="header">
  <nav class="navbar">
    <div class="logo">
      <img src="/img/fixlat.svg" alt="Fixlat Logo" />
    </div>
    <ul class="nav-links">
      <li><a href="#hero">Inicio</a></li>
      <li><a href="#soluciones">Soluciones</a></li>
      <li><a href="#aliados">Aliados</a></li>
      <li><a href="#cobertura">Cobertura</a></li>
      <li><a href="#vision2030">Visión 2030</a></li>
      <li><a href="#contacto">Contacto</a></li>
    </ul>
  </nav>
</header>

<style>
  .header {
    background: #fff;
    box-shadow: 0 2px 12px rgba(10, 37, 64, 0.07);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  .navbar {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 68px;
  }
  .logo {
    display: flex;
    align-items: center;
    gap: 150px;
    font-size: 1.3rem;
    font-weight: 900;
    color: #0a2540;
  }
  .logo img {
    height: 68px;
  }
  .nav-links {
    display: flex;
    gap: 28px;
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .nav-links a {
    color: #0a2540;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    transition: color 0.2s;
  }
  .nav-links a:hover {
    color: #1e90ff;
  }
  @media (max-width: 800px) {
    .navbar {
      flex-direction: column;
      height: auto;
      padding: 12px 12px;
    }
    .nav-links {
      gap: 16px;
      flex-wrap: wrap;
      justify-content: center;
    }
  }
</style>
