<section class="soluciones" id="soluciones">
  <h2>Nuestras Soluciones</h2>
  <div class="soluciones-grid">
    <div class="solucion-card">
      <img src="/img/iot.png" alt="IoT" class="icon" />
      <h3>IoT y Smart Metering</h3>
      <p>Implementación de redes inteligentes para la medición y gestión eficiente de agua y energía.</p>
    </div>
    <div class="solucion-card">
      <img src="/img/consulto.png" alt="Consultoría" class="icon" />
      <h3>Consultoría Especializada</h3>
      <p>Asesoría estratégica y técnica para empresas de servicios públicos y gobiernos.</p>
    </div>
    <div class="solucion-card">
      <img src="/img/analytics.png" alt="Analytics" class="icon" />
      <h3>Analítica & Big Data</h3>
      <p>Soluciones de análisis avanzado para la toma de decisiones basada en datos.</p>
    </div>
    <div class="solucion-card">
      <img src="/img/gestion.png" alt="Gestión" class="icon" />
      <h3>Gestión Integral de Proyectos</h3>
      <p>Desde la conceptualización hasta la operación, acompañamos todo el ciclo de vida del proyecto.</p>
    </div>
  </div>
</section>

<style>
.icon {
  background: transparent;
  box-shadow: none;
  border: none;
  border-radius: 16px;
  width: 90px;
  height: 90px;
  object-fit: contain;
  display: block;
  margin: 0 auto 18px auto;
}
.soluciones {
  background: #f7fbfd;
  color: #0a2540;
  padding: 64px 0 48px 0;
  text-align: center;
}
.soluciones h2 {
  font-size: 2.1rem;
  font-weight: 900;
  margin-bottom: 36px;
  color: #0a2540;
}
.soluciones-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 32px;
  justify-items: center;
}
.solucion-card {
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(10,37,64,0.08);
  padding: 32px 18px 24px 18px;
  min-width: 220px;
  max-width: 320px;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: box-shadow 0.3s, transform 0.3s;
  opacity: 0;
  transform: translateY(40px);
  animation: fadeinUp 1s cubic-bezier(.4,0,.2,1) forwards;
}
.solucion-card:hover {
  box-shadow: 0 8px 32px rgba(255,140,0,0.15), 0 2px 8px rgba(0,0,0,0.08);
  transform: translateY(-6px) scale(1.04);
}
@keyframes fadeinUp {
  to {
    opacity: 1;
    transform: none;
  }
}
.icon {
  width: 90px;
  height: 90px;
  object-fit: contain;
  border-radius: 16px;
  background: transparent;
  box-shadow: none;
  margin-bottom: 18px;
  border: none;
}
.solucion-card h3 {
  font-size: 1.15rem;
  font-weight: 700;
  margin-bottom: 10px;
  color: #1e90ff;
}
.solucion-card p {
  font-size: 1rem;
  color: #0a2540;
}
</style>
