<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
      <Index />
    </div>
    <router-view />
  </div>
</template>
<script>
import Index from "./views/rooms/Index.vue";
export default {
  components: { Index },
};
</script>
<style lang="scss">
</style>
