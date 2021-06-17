<template>
  <!-- Esta es la seccion del footer -->
  <footer class="footer">
    <h2>Detalles de contacto</h2>
    <div class="footer-details">
      <div class="footer-details-content">
        <h4>EMAIL</h4>
        <p class="footer-details-content-email"></p>
      </div>
      <div class="footer-details-content">
        <h4>Celular</h4>
        <p>+51 988 400 110</p>
      </div>
      <div class="footer-details-content">
        <h4>Dirección</h4>
        <p>Asoc. de Vivienda los claveles de Lurín Mz. N Lt. 13</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "PxFooter",
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/Footer/footer.scss";
</style>
