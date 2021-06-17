<template>
  <header
    :class="{
      header: true,
      fixed: fixedHeader,
    }"
  >
    <div
      :class="{ 'burger-button': true, 'is-active': openMenuState }"
      @click="handleOpenMenuMobile()"
    >
      <font-awesome-icon v-if="!openMenuState" icon="bars" />
      <font-awesome-icon v-else icon="times" />
    </div>
    <nav
      :class="{
        menu: true,
        'is-active': openMenuState,
      }"
    >
      <ul
        :class="{
          'menu-effect-circle': true,
          'is-active': openMenuState,
        }"
      >
        <li
          class="menu-item"
          v-for="(menu, index) in menuImtesState"
          :key="index"
        >
          <router-link
            class="menu-link"
            :to="menu.to"
            v-text="menu.text"
            @click="handleDissapearMenu"
          ></router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faBars, faTimes } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { reactive, ref, toRefs, onMounted } from "vue";

library.add(faBars, faTimes);

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

    const openMenuState = ref(false);
    let fixedHeader = ref(false);
    const body = ref(null);

    onMounted(() => {
      document.addEventListener("scroll", () => {
        let y = window.scrollY;
        y > 56 ? (fixedHeader.value = true) : (fixedHeader.value = false);
      });
    });

    const handleOpenMenuMobile = () =>
      (openMenuState.value = !openMenuState.value);

    const handleDissapearMenu = () => {
      openMenuState.value = !openMenuState.value;
    };

    return {
      menuImtesState,
      fixedHeader,
      handleOpenMenuMobile,
      openMenuState,
      handleDissapearMenu,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/Header/header.scss";
</style>
