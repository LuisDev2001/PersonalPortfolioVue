<template>
  <div class="home">
    <PxBanner />
  </div>
</template>

<script>
// @ is an alias to /src
import PxBanner from "@/components/Home/PxBanner";

export default {
  name: "Home",
  components: {
    PxBanner,
  },
};
</script>
