<template>
  <section class="resume">
    <h2 class="generic-title">Mi <b>Resumen</b></h2>
    <section class="resume-container">
      <section class="education">
        <h2 class="resume-container__title">Educación</h2>
        <div class="resume-wrapper">
          <article
            class="resume-wrapper-cards"
            v-for="(education, index) in infoEducation"
            :key="index"
          >
            <h4>
              <font-awesome-icon icon="calendar-alt" />
              {{ education.year }}
            </h4>
            <h2 v-text="education.typeEducation"></h2>
            <p v-text="education.description"></p>
            <span v-text="education.address"></span>
          </article>
        </div>
      </section>
      <section class="experiencie">
        <h2 class="resume-container__title">Experiencia</h2>
        <div class="resume-wrapper">
          <article
            class="resume-wrapper-cards"
            v-for="(experiencie, index) in infoExperience"
            :key="index"
          >
            <h4>
              <font-awesome-icon icon="calendar-alt" />
              {{ experiencie.date }}
            </h4>
            <h2 v-text="experiencie.typeExp"></h2>
            <p v-text="experiencie.description"></p>
            <span v-text="experiencie.address"></span>
          </article>
        </div>
      </section>
    </section>
  </section>
</template>

<script>
import { ref } from "vue";

import { library } from "@fortawesome/fontawesome-svg-core";
import { faCalendarAlt } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

library.add(faCalendarAlt);

export default {
  name: "PxInfoResume",
  components: {
    FontAwesomeIcon,
  },
  setup() {
    const infoEducation = ref([
      {
        year: "2007 - 2013",
        typeEducation: "Educación primaria",
        description: `Estudié en la institución educativa 6031 Santa María de Lurín,
                      estuve por 6 años estudiando mi primaria, educandome y formandome
                      en valores.`,
        address: "Perú, Lima, Lurín",
      },
      {
        year: "2014 - 2018",
        typeEducation: "Educación secundaria",
        description: `Estudié en la institución educativa José Faustino Sánchez Carrión
                      de Lurín, permanecí por 5 años estudiando mi secundaria. En mi
                      adolecencia lleve talleres de Computación y Mecánica de producción
                      dadas por mi institución educativa.`,
        address: "Perú, Lima, Lurín",
      },
      {
        year: "2017 - Presente",
        typeEducation: "Educación técnico superior - Computación e Informática",
        description: `Actualmente estudio en el instituto tecnico llamado SENATI,
                      gracias a una beca de la institución PRONABEC obtuve una beca de
                      educación tecnica, escogí estudiar la carrera de desarrollo de
                      aplicaciones web en la sede de San Juan de Miraflores, aprendiendo
                      cursos de informática básica y avanzada, en esta etapa me encantó
                      perdidamente el desarrollo web, actualmente sigo en formación para
                      poder sacar mi título como técnico a nombre de la nación.`,
        address: "Perú, Lima, San Juan de Miraflores",
      },
      {
        year: "30 de Febrero 2020 - 25 de Julio 2020",
        typeEducation: "Especialización",
        description: `Lleve una especialización en desarrollo web Front-end, lleve el
                      bootcamp en las instalaciones del instituto Idat, y la encargada
                      de formarme como frontend developer fue PachaQtec escuela de
                      coding, aprendi a desarrollar web´s con buenas prácticas,
                      nomenclaturas css, arquitecturas css, aprendi a escribir codigo en
                      vanilla js, y me especialicé en desarrollo front-end con VUE JS,
                      fue un reto muy chevere y del cual obtuve conocimientos muy
                      importantes para el desarrollo de mi carrera como front-end
                      developer.`,
        address: "Perú, Lima, San Juan de Miraflores",
      },
    ]);

    const infoExperience = ref([
      {
        date: "26 de julio de 2019 – 11 de agosto de 2019",
        typeExp: "Voluntario en Tecnologia (Backup)",
        description: `Fuí voluntario de tecnologia en los juego panamericanos Lima 2019,
                      trabaje con la gente de ATOS encargados del sistema de puntuación
                      de la sede de Surf - Punta Rocas, aprendí mucho en esta grata a
                      experiencia.`,
        address: "Perú, Lima, Lurín",
      },
      {
        date: "17 de Febrero - Presente",
        typeExp: "Web Developer Front-end",
        description: `Actualmente llevo 8 meses como desarrollador web Frontend en la
                      empresa Avatar Global, al incio fue un poco dificil adaptarme al
                      tipo de trabajo, con el pasar del tiempo fui agarrando la onda y
                      pues cada dia que pasa es un reto más. Si lees esto desde aqui te
                      digo, no te rindas y nunca dejes de aprender. La única manera de
                      progresar en este mundo del desarrollo web es seguir aprendiendo.`,
        address: "Perú, San Isidro",
      },
    ]);
    return {
      infoEducation,
      infoExperience,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/Components/Resume/_resume.scss";
</style>
