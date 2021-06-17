<template>
  <PxHeader />
  <PxReturTop />
  <router-view />
</template>

<script>
import PxHeader from "@/components/PxHeader";
import PxReturTop from "@/components/PxReturTop";

export default {
  name: "App",
  components: {
    PxHeader,
    PxReturTop,
  },
};
</script>
<style lang="scss">
@import "~@/assets/sass/main.scss";
</style>
