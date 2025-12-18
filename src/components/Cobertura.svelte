<section class="cobertura" id="cobertura">
  <h2>Impacto y Cobertura</h2>
  <p class="cobertura-desc">Conectando utilidades desde México hasta el Cono Sur.</p>
  <div class="cobertura-grid">
    <div class="cob-card principal">
      <span class="pais">🇨🇴 Colombia</span>
      <div class="detalle">Aliado estratégico del MinTIC para la plataforma "PAIS".<br>Trabajo directo e indirecto con 261 empresas de servicios públicos (PyMES).</div>
    </div>
    <div class="cob-card">
      <span class="pais">🇲🇽 México</span>
      <div class="detalle">Proyectos con 12+ utilidades medianas y grandes.<br>Consultores para 36+ proyectos de distribución de agua privada.</div>
    </div>
    <div class="cob-card">
      <span class="pais">🇵🇪 Perú</span>
      <div class="detalle">Socio y consultor del mayor distribuidor de medidores inteligentes del país.</div>
    </div>
    <div class="cob-card">
      <span class="pais">🌎 Regional</span>
      <div class="detalle">Soporte técnico a servicios públicos en Chile, Brasil y Uruguay.</div>
    </div>
    <div class="cob-card expansion">
      <span class="pais">📈 En Expansión</span>
      <div class="detalle">Paraguay 🇵🇾, Panamá 🇵🇦, República Dominicana 🇩🇴, Guatemala 🇬🇹</div>
    </div>
  </div>
</section>

<style>
.cobertura {
  background: #f7fafc;
  padding: 60px 0 40px 0;
  text-align: center;
}
.cobertura h2 {
  color: #0a2540;
  font-size: 2.1rem;
  font-weight: 800;
  margin-bottom: 10px;
}
.cobertura-desc {
  color: #1e90ff;
  font-size: 1.1rem;
  margin-bottom: 32px;
}
.cobertura-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  justify-content: center;
}
.cob-card {
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(10,37,64,0.08);
  padding: 32px 18px 24px 18px;
  min-width: 220px;
  max-width: 320px;
  flex: 1 1 220px;
  text-align: left;
  transition: box-shadow 0.3s, transform 0.3s;
  opacity: 0;
  transform: translateY(40px);
  animation: fadeinUp 1s cubic-bezier(.4,0,.2,1) forwards;
}
.cob-card:hover {
  box-shadow: 0 8px 32px rgba(255,140,0,0.15), 0 2px 8px rgba(0,0,0,0.08);
  transform: translateY(-6px) scale(1.04);
}
@keyframes fadeinUp {
  to {
    opacity: 1;
    transform: none;
  }
}
.cob-card.principal {
  border: 2px solid #1e90ff;
}
.cob-card .pais {
  font-size: 1.15rem;
  font-weight: bold;
  color: #0072c6;
}
.cob-card .detalle {
  font-size: 1rem;
  color: #23395d;
  margin-top: 8px;
}
.cob-card.expansion {
  background: #eaf6fb;
  border: 1.5px dashed #1e90ff;
}
</style>
