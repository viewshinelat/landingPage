<script>
  let nombre = "";
  let email = "";
  let mensaje = "";
  let loading = false;
  let statusMessage = "";
  let statusType = ""; // 'success' or 'error'

  async function handleSubmit(e) {
    e.preventDefault();

    // Reset status
    statusMessage = "";
    statusType = "";
    loading = true;

    try {
      // Send email using EmailJS
      const response = await emailjs.send(
        "service_rdoahqy", // Service ID
        "template_34xe98p", // Template ID
        {
          from_name: nombre,
          from_email: email,
          from_message: mensaje,
        }
      );

      console.log("Email sent successfully:", response);

      // Show success message
      statusMessage = "¡Gracias por contactarnos! Te responderemos pronto.";
      statusType = "success";

      // Reset form
      nombre = "";
      email = "";
      mensaje = "";
    } catch (error) {
      console.error("Error sending email:", error);
      statusMessage =
        "Hubo un error al enviar el mensaje. Por favor, intenta nuevamente.";
      statusType = "error";
    } finally {
      loading = false;
    }
  }
</script>

<section class="contacto" id="contacto">
  <h2>Contacto</h2>
  <form class="contact-form" on:submit={handleSubmit}>
    <div class="form-row">
      <input
        type="text"
        placeholder="Nombre"
        bind:value={nombre}
        required
        disabled={loading}
      />
      <input
        type="email"
        placeholder="Correo electrónico"
        bind:value={email}
        required
        disabled={loading}
      />
    </div>
    <textarea
      placeholder="¿En qué podemos ayudarte?"
      bind:value={mensaje}
      required
      disabled={loading}
    ></textarea>
    <button type="submit" disabled={loading}>
      {loading ? "Enviando..." : "Enviar mensaje"}
    </button>

    {#if statusMessage}
      <div class="status-message {statusType}">
        {statusMessage}
      </div>
    {/if}
  </form>
  <div class="contact-info">
    <div><strong>Email:</strong> comercial@fixlat.com</div>
    <div><strong>Teléfono:</strong> +57 310 415 4049</div>
    <div>
      <strong>Oficina:</strong> Cl. 6 Nte. #1-42, Granada, Cali, Valle del Cauca,
      Colombia
    </div>
  </div>
</section>

<style>
  .contacto {
    text-align: center;
    padding: 64px 0 32px 0;
    box-shadow: 0 2px 16px rgba(10, 37, 64, 0.08);
    border-radius: 18px;
    color: #0a2540;
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
    box-shadow: 0 2px 12px rgba(10, 37, 64, 0.08);
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
  button[type="submit"]:hover:not(:disabled) {
    background: #7ee6e6;
    color: #0a2540;
  }
  button[type="submit"]:disabled {
    background: #ccc;
    cursor: not-allowed;
    opacity: 0.6;
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
  .status-message {
    margin-top: 12px;
    padding: 12px;
    border-radius: 6px;
    font-weight: 600;
    text-align: center;
  }
  .status-message.success {
    background-color: #d4edda;
    color: #155724;
    border: 1px solid #c3e6cb;
  }
  .status-message.error {
    background-color: #f8d7da;
    color: #721c24;
    border: 1px solid #f5c6cb;
  }
</style>
