<template>
  <!-- Esta es la seccion de contacto -->
  <section class="contact">
    <h2 class="generic-title"><b>Contáctame</b></h2>
    <form
      action="./mail/sendMail.php"
      method="POST"
      class="contact-form"
      id="js_form-data"
    >
      <div>
        <input
          type="text"
          required
          placeholder="Tu nombre"
          name="name"
          pattern="[a-z][A-Z]"
        />
      </div>
      <div>
        <input type="email" required placeholder="Tu correo" name="email" />
      </div>
      <div>
        <input
          type="tel"
          required
          placeholder="Tu numero de celular"
          name="phone"
          maxlength="9"
          pattern="[0-9]"
        />
      </div>
      <div>
        <textarea
          cols="30"
          rows="10"
          placeholder="Escribe un mensaje"
          name="message"
        ></textarea>
      </div>
      <div>
        <button type="submit" class="btn btn-primary" id="js_send-mail">
          Enviar mensaje
        </button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  name: "PxFormContact",
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/Contact/form.scss";
</style>
