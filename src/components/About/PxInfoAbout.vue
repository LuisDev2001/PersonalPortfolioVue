<template>
  <section class="aboutMe" id="about-me">
    <picture>
      <img loading="lazy" src="/assets/img/aboutMe.jpg" alt="About me" />
    </picture>
    <section class="aboutMe-information">
      <h2 class="generic-title">Sobre <b>Mí</b></h2>
      <p>
        Nací un 12 de Setiembre del 2001 en la maternidad de Lima, mis padres me
        educaron y cuidaron. Actualmente vivo en el distrito de Lurin, crecí en
        contacto desde muy chico con una computadora, desde el inicio me
        gustaron los videojuegos y poco a poco fui introduciendome mas en este
        maravilloso mundo de la computacion e informática.
      </p>
      <p>
        En mis tiempos libres me gusta tocar guitarra, escuchar musica, ver
        videos de youtube, pasar el rato en redes sociales, generar contenido
        para mi canal de youtube, salir a caminar para despejar la mente y
        obviamente desarrollar web / challenge´s en html, css, javascript ó Vue
        JS.
      </p>
      <section class="aboutMe-information-buttons">
        <div>
          <a href="#" class="btn btn-primary"> Contratame </a>
        </div>
        <div>
          <a
            href="https://www.linkedin.com/in/luis-aldair-quispe-rios-8b6096161/"
            target="_blank"
            class="btn btn-secondary"
          >
            Ver CV
          </a>
        </div>
      </section>
    </section>
  </section>
</template>

<script>
export default {
  name: "PxInfoAbout",
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/About/about.scss";
</style>
