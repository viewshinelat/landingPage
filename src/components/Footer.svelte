<footer class="footer">
  <!-- Logo Section with Light Background -->
  <div class="footer-logo-section">
    <div class="footer-logo">
      <img src="/img/fixlat.svg" alt="Fixlat Logo" />
    </div>
  </div>

  <!-- Links Section with Dark Background -->
  <div class="footer-links-section">
    <div class="footer-content">
      <div class="footer-links">
        <a href="#soluciones">Soluciones</a>
        <a href="#aliados">Aliados</a>
        <a href="#cobertura">Cobertura</a>
        <a href="#vision2030">Visión 2030</a>
        <a href="#contacto">Contacto</a>
      </div>
      <div class="footer-copy">
        &copy; {new Date().getFullYear()} Fixlat. Todos los derechos reservados.
      </div>
    </div>
  </div>
</footer>

<style>
  .footer {
    width: 100%;
  }

  /* Logo Section - Light Background */
  .footer-logo-section {
    background: linear-gradient(135deg, #d7e4f7 0%, #b1cef1 100%);
    padding: 0;
    text-align: center;
  }

  .footer-logo {
    display: inline-flex;
    align-items: center;
    gap: 16px;
    font-size: 2.5rem;
    font-weight: 900;
    color: #0a2540;
  }

  .footer-logo img {
    height: 140px;
  }

  /* Links Section - Dark Background */
  .footer-links-section {
    background: #0a2540;
    color: #fff;
    padding: 40px 0 70px 0;
    text-align: center;
  }

  .footer-content {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px;
  }

  .footer-links {
    display: flex;
    gap: 22px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .footer-links a {
    color: #7ee6e6;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    transition: color 0.2s;
  }

  .footer-links a:hover {
    color: #1e90ff;
  }

  .footer-copy {
    font-size: 0.95rem;
    color: #b2e0e0;
    margin-top: 8px;
  }

  @media (max-width: 600px) {
    .footer-logo {
      flex-direction: column;
      gap: 12px;
    }

    .footer-logo img {
      height: 80px;
    }

    .footer-links {
      gap: 16px;
      font-size: 0.9rem;
    }
  }
</style>
