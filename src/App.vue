<template>
  <PxHeader />
  <PxReturTop />
  <router-view v-slot="{ Component }">
    <transition name="mode-fade" mode="out-in">
      <component :is="Component" />
    </transition>
  </router-view>
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
@import "~@/assets/sass/_main.scss";
</style>
