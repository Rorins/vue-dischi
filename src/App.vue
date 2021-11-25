<template>
  <div id="app">
    <!--Header-->
    <Header />
    <!--Main-->
    <Disks />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Disks from '@/components/Disks.vue';


export default {
  name: "App",
  components: {
    Header,
    Disks,
  },
};
</script>

<style lang="scss">
@import '@/styles/globals';
</style>
