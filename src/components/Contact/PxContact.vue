<template>
  <section class="contact-me">
    <h2 class="generic-title">Ponerse en <b>Contacto</b></h2>

    <section class="contact-me-wrapper">
      <PxFormContact />

      <PxFooter />
    </section>

    <PxSocialMedia />
  </section>
</template>

<script>
import PxFooter from "@/components/PxFooter";
import PxFormContact from "@/components/Contact/PxFormContact";
import PxSocialMedia from "@/components/Contact/PxSocialMedia";

export default {
  name: "PxContact",
  components: {
    PxFooter,
    PxFormContact,
    PxSocialMedia,
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/Components/Contact/_globalContact.scss";
</style>
