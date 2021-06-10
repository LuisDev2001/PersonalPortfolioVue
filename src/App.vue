<template>
  <PxHeader />
  <router-view />
</template>

<script>
import PxHeader from "@/components/PxHeader";

export default {
  name: "App",
  components: {
    PxHeader,
  },
};
</script>
<style lang="scss">
@import "~@/assets/sass/main.scss";
</style>
