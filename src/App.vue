<template>
  <HeaderComponent />
  <MainComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';

export default {
  components: {
    HeaderComponent,
    MainComponent

  }
}

</script>

<style lang="scss" scoped>
@use './assets/style/variables.scss' as *;
@use './assets/style/general.scss' as *;
</style>