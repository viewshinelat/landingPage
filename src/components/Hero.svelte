<section class="hero" id="hero">
  <div class="hero-content">
    <div class="hero-text">
      <h1>Soluciones inteligentes para la gestión del agua</h1>
      <p>
        Impulsamos la transformación digital de servicios públicos en
        Latinoamérica y el mundo, integrando tecnología, consultoría y analítica
        avanzada.
      </p>
      <a href="#contacto" class="cta">Contáctanos</a>
    </div>
    <div class="hero-media">
      <img src="/svg/hero-section.svg" alt="Ilustración Hero" class="hero-3d" />
    </div>
    <style>
      .hero-3d {
        width: 100%;
        max-width: 600px;
        border-radius: 16px;
        box-shadow: 0 4px 24px rgba(10, 37, 64, 0.13);
        background: #0a2540;
        margin-top: 12px;
        animation: fadeinImg 1.2s cubic-bezier(0.4, 0, 0.2, 1) forwards;
        opacity: 0;
      }
      @keyframes fadeinImg {
        to {
          opacity: 1;
        }
      }
    </style>
  </div>
</section>

<style>
  .hero {
    background: linear-gradient(120deg, #0a2540 60%, #1e90ff 100%);
    color: #fff;
    padding: 64px 0 32px 0;
    min-height: 480px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden; /* Evita scrollbars por animaciones */
  }
  .hero-content {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    gap: 48px;
    width: 100%;
    justify-content: space-between;
  }
  .hero-text {
    flex: 1 1 340px;
    min-width: 300px;
  }
  .hero-text h1 {
    font-size: 2.5rem;
    font-weight: 900;
    margin-bottom: 18px;
    color: #fff;
  }
  .hero-text p {
    font-size: 1.15rem;
    margin-bottom: 28px;
    color: #e0f7fa;
  }
  .cta {
    display: inline-block;
    background: #1e90ff;
    color: #fff;
    font-weight: 700;
    padding: 12px 32px;
    border-radius: 8px;
    text-decoration: none;
    font-size: 1.1rem;
    transition: background 0.2s;
  }
  .cta:hover {
    background: #7ee6e6;
    color: #0a2540;
  }
  .hero-media {
    flex: 1 1 340px;
    min-width: 300px;
    min-height: 320px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .hero-media video {
    width: 100%;
    max-width: 420px;
    border-radius: 16px;
    box-shadow: 0 4px 24px rgba(10, 37, 64, 0.13);
    background: #0a2540;
  }
  @media (max-width: 1100px) {
    .hero-content {
      flex-direction: column;
      gap: 32px;
      text-align: center;
    }
    .hero-media,
    .hero-text {
      min-width: 0;
    }
    .hero-media {
      margin-top: 24px;
    }
  }
</style>
