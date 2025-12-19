<section class="contacto" id="contacto">
  <h2>Contacto</h2>
  <form class="contact-form">
    <div class="form-row">
      <input type="text" placeholder="Nombre" required />
        <input type="email" placeholder="Correo electrónico" required />
    </div>
    <textarea placeholder="¿En qué podemos ayudarte?" required></textarea>
    <button type="submit">Enviar mensaje</button>
  </form>
  <div class="contact-info">
    <div><strong>Email:</strong> comercial@fixlat.com</div>
    <div><strong>Teléfono:</strong> +57 310 415 4049</div>
    <div><strong>Oficina:</strong> Carrera 41 #13C-34, Cali, Valle del Cauca, Colombia</div>
  </div>
</section>

<style>
html, body {
  max-width: 100vw;
  overflow-x: hidden;
}
.contacto {
  background: #f7fbfd;
  color: #0a2540;
  padding: 64px 0 48px 0;
  text-align: center;
}
.contacto h2 {
  font-size: 2.1rem;
  font-weight: 900;
  margin-bottom: 28px;
  color: #0a2540;
}
.contact-form {
  max-width: 480px;
  margin: 0 auto 32px auto;
  display: flex;
  flex-direction: column;
  gap: 18px;
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(10,37,64,0.08);
  padding: 32px 24px 24px 24px;
}
  .form-row {
    display: flex;
    gap: 12px;
  }
  .form-row input {
    flex: 1;
    padding: 12px;
    border: 1px solid #b2e0e0;
    border-radius: 6px;
    font-size: 1rem;
  }

  @media (max-width: 600px) {
    .form-row {
      flex-direction: column;
      gap: 8px;
    }
    .form-row input {
      width: 100%;
    }
  }
textarea {
  padding: 12px;
  border: 1px solid #b2e0e0;
  border-radius: 6px;
  font-size: 1rem;
  min-height: 80px;
  resize: vertical;
}
button[type="submit"] {
  background: #1e90ff;
  color: #fff;
  font-weight: 700;
  padding: 12px 0;
  border: none;
  border-radius: 8px;
  font-size: 1.1rem;
  margin-top: 8px;
  cursor: pointer;
  transition: background 0.2s;
}
button[type="submit"]:hover {
  background: #7ee6e6;
  color: #0a2540;
}
.contact-info {
  margin-top: 18px;
  color: #0a2540;
  font-size: 1.05rem;
  display: flex;
  flex-direction: column;
  gap: 6px;
  align-items: center;
}
</style>
