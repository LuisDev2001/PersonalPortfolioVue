<template>
  <header class="header" id="js_header">
    <div class="burger-button" id="js_burger-button">
      <font-awesome-icon icon="bars" />
    </div>
    <nav class="menu">
      <ul class="menu-list" id="js_menu">
        <li
          class="menu-item"
          v-for="(menu, index) in menuImtesState"
          :key="index"
        >
          <router-link
            class="menu-link"
            :to="menu.to"
            v-text="menu.text"
          ></router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faBars } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { reactive, ref, toRefs } from "vue";
library.add(faBars);

export default {
  name: "PxHeader",
  components: {
    FontAwesomeIcon,
  },
  setup() {
    const menuImtesState = ref([
      {
        to: "/",
        name: "",
        text: "Inicio",
      },
      {
        to: "/about-me",
        name: "",
        text: "Sobre mí",
      },
      {
        to: "/resume-me",
        name: "",
        text: "Resumen",
      },
      {
        to: "/portfolio",
        name: "",
        text: "Portafolio",
      },
      {
        to: "/contact-me",
        name: "",
        text: "Contactame",
      },
    ]);

    return {
      menuImtesState,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/header/header.scss";
</style>
