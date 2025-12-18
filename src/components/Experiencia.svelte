<section class="experiencia" id="experiencia">
  <h2>Experiencia y Proyectos Destacados</h2>
  <div class="exp-grid">
    <div class="exp-card">
      <h3>Alianzas Internacionales</h3>
      <p><b>Fixlat S.A.S</b> trabaja con <b>Viewshine</b>, empresa líder china en sensores de agua y gas. Gestionamos dispositivos en:</p>
      <ul>
        <li>Chile (Punta Cana)</li>
        <li>Perú (Lima)</li>
        <li>México (Ciudad de México)</li>
        <li>Colombia (Cali y Funes, Nariño)</li>
      </ul>
      <p class="exp-note">Datos gestionados en bases internacionales y locales.</p>
    </div>
    <div class="exp-card">
      <h3>Proyectos Tecnológicos</h3>
      <ul>
        <li><b>MITIC (Funes, Nariño):</b> Sensores de aforo para personas y vehículos, integrando datos a <b>Plataforma País</b> y <b>Datos Abiertos</b> de MINTIC Colombia.</li>
        <li><b>Smart:</b> Consultor de información para sensores, desarrollado para Medileser, con filtros y visualización Power BI.</li>
        <li><b>Web Services:</b> Extracción de datos para Medileser, Veolia (España) y otros clientes.</li>
        <li><b>Geolocalizador:</b> Ubicación de sensores, mapas de calor y conectividad con gateways.</li>
      </ul>
    </div>
    <div class="exp-card">
      <h3>Capacidades Avanzadas</h3>
      <ul>
        <li>Reportes en tiempo real y alertas inteligentes (flujo inverso, caídas de conexión, etc.).</li>
        <li>Integración con plataformas de análisis y visualización.</li>
        <li>Soporte para diferentes sensores y protocolos de comunicación.</li>
      </ul>
    </div>
  </div>
</section>

<style>
.experiencia {
  background: #eaf1f8;
  padding: 60px 20px 40px 20px;
  max-width: 1200px;
  margin: 0 auto 48px auto;
  border-radius: 18px;
}
.experiencia h2 {
  text-align: center;
  font-size: 2.1rem;
  font-weight: 800;
  color: #0a2540;
  margin-bottom: 40px;
}
.exp-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  justify-content: center;
}
.exp-card {
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 4px 24px rgba(44,62,80,0.08);
  padding: 36px 28px 28px 28px;
  flex: 1 1 320px;
  min-width: 260px;
  max-width: 370px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
    transition: box-shadow 0.3s, transform 0.3s;
    opacity: 0;
    transform: translateY(40px);
    animation: fadeinUp 1s cubic-bezier(.4,0,.2,1) forwards;
}
.exp-card:hover {
  transform: translateY(-6px) scale(1.03);
  box-shadow: 0 8px 32px rgba(44,62,80,0.13);
  }
}
@keyframes fadeinUp {
  to {
    opacity: 1;
    transform: none;
  }
}
.exp-card h3 {
  color: #ff6f3c;
  font-size: 1.18rem;
  font-weight: 700;
  margin-bottom: 12px;
}
.exp-card ul {
  margin-left: 18px;
  margin-bottom: 10px;
  color: #23395d;
  font-size: 1.05rem;
}
.exp-card p, .exp-card .exp-note {
  color: #23395d;
  font-size: 1.05rem;
  margin-bottom: 10px;
}
.exp-note {
  font-size: 0.98rem;
  color: #1769aa;
  font-style: italic;
}
@media (max-width: 900px) {
  .exp-grid {
    flex-direction: column;
    gap: 24px;
    align-items: center;
  }
}
</style>
