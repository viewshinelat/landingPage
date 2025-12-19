<section class="cobertura" id="cobertura">
  <h2>Impacto y Cobertura</h2>
  <p class="cobertura-desc">Conectando utilidades desde México hasta el Cono Sur.</p>
  <div class="cobertura-grid">
    <div class="cob-card principal">
      <span class="pais">Colombia</span>
      <div class="detalle-flex">Aliado estratégico del MinTIC para la plataforma "PAIS".<br>Trabajo directo e indirecto con 261 empresas de servicios públicos (PyMES).<img src="/img/Colombia.png" alt="Colombia" class="img-bandera" /></div>

    </div>

    <div class="cob-card">
      <span class="pais">México</span>
      <div class="detalle-flex">Proyectos con 12+ utilidades medianas y grandes.<br>Consultores para 36+ proyectos de distribución de agua privada.<img src="/img/Mexico.png" alt="México" class="img-bandera" /></div>
    </div>
    <div class="cob-card">
      <span class="pais">Perú</span>
      <div class="detalle-flex">Socio y consultor del mayor distribuidor de medidores inteligentes del país.<img src="/img/Peru.png" alt="Perú" class="img-bandera" /></div>
    </div>
    <div class="cob-card expansion">
      <span class="pais">🌎 Regional y Países en Expansión</span>
      <div class="detalle-flex">
        Soporte técnico a servicios públicos en Chile, Brasil y Uruguay.<br>
        <strong>En Expansión:</strong> Paraguay, Panamá, República Dominicana, Guatemala<img src="/img/latam.png" alt="Latam" class="img-bandera" />
      </div>
    </div>
  </div>
</section>

<style>
.img-bandera {
  display: block;
  margin: 18px auto 0 auto;
  width: 90px;
  height: 90px;
  object-fit: contain;
  border-radius: 16px;
  background: transparent;
  box-shadow: none;
  border: none;
}
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
  align-items: stretch;
}
/* Asegura que todas las tarjetas tengan la misma altura y las banderas queden abajo */
/* Todas las tarjetas con la misma altura visual */
/* Todas las tarjetas con altura visual uniforme y banderas a 10px del fondo */
/* Todas las tarjetas con altura visual uniforme y banderas a 3px del fondo */
.cob-card {
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(10,37,64,0.08);
  padding: 32px 18px 24px 18px;
  min-width: 220px;
  max-width: 320px;
  flex: 1 1 220px;
  min-height: 240px;
  height: 100%;
  padding-bottom: 3px;
  text-align: left;
  transition: box-shadow 0.3s, transform 0.3s;
  opacity: 0;
  transform: translateY(40px);
  animation: fadeinUp 1s cubic-bezier(.4,0,.2,1) forwards;
  display: flex;
  flex-direction: column;
  height: 100%;
  flex: 1 1 0;
}
.detalle-flex {
  flex: 1 1 0;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  height: 100%;
}
.img-bandera {
  margin-top: auto;
  margin-bottom: 24000px;
  padding-bottom: 0;
  align-self: center;
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
  /* Sin borde azul para uniformidad */
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
.detalle-flex {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 180px;
}
.img-bandera {
  margin-top: auto;
  margin-bottom: 0;
}
.cob-card.expansion {
  background: #fff;
  border: none;
}
</style>
