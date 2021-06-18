<template>
  <!-- Esta es la seccion de contacto -->
  <section class="contact">
    <h2 class="generic-title"><b>Contáctame</b></h2>
    <form
      class="contact-form"
      ref="jsFormContact"
      @submit.prevent="handleSubmitForm"
    >
      <div>
        <input
          type="text"
          placeholder="Tu nombre"
          v-model="formDataContact.name"
          required
        />
      </div>
      <div>
        <input
          type="email"
          placeholder="Tu correo"
          v-model="formDataContact.email"
          required
        />
      </div>
      <div>
        <input
          type="tel"
          placeholder="Tu numero de celular"
          v-model="formDataContact.phone"
          required
          maxlength="9"
        />
      </div>
      <div>
        <textarea
          cols="30"
          rows="10"
          placeholder="Escribe un mensaje"
          v-model="formDataContact.message"
          required
        ></textarea>
      </div>
      <div>
        <button type="submit" class="btn btn-primary" id="js_send-mail">
          Enviar mensaje
        </button>
      </div>
    </form>

    <PxModal
      title="Gracias!"
      message="En breve te escribiré, muchas gracias por visitar mi portafolio"
      textButton="OK"
      :isOpenModal="isOpenModalThnx"
    />
  </section>
</template>

<script>
import PxModal from "@/components/PxModal";

import { ref } from "vue";
export default {
  name: "PxFormContact",
  components: {
    PxModal,
  },
  setup() {
    const formDataContact = ref({
      name: "",
      email: "",
      message: "",
      phone: "",
    });
    const isOpenModalThnx = ref(false);
    const jsFormContact = ref(null);
    const handleSubmitForm = async () => {
      const API = "https://formspree.io/f/mjvjrpjz";
      const response = await fetch(API, {
        method: "POST",
        body: JSON.stringify(formDataContact.value),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      });
      if (response.ok) {
        isOpenModalThnx.value = true;
        formDataContact.value.name = "";
        formDataContact.value.email = "";
        formDataContact.value.message = "";
        formDataContact.value.phone = "";
      }
    };

    return {
      handleSubmitForm,
      jsFormContact,
      formDataContact,
      isOpenModalThnx,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/Contact/form.scss";
</style>
