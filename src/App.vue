<template>
  <main id="app">
    <router-view class="view" />
    <Cover />
  </main>
</template>
<script>
import Cover from './components/Cover.vue'

export default {
  components: { Cover }
}
</script>
<style lang="scss" scoped>
#app {
  position: relative;
  display: grid;
  grid-template-columns: 50% 50%;
  height: 100%;
  margin: 0 auto;
  text-align: center;

  @media screen and (max-width: 1000px) {
    grid-template-columns: 100%;
    grid-template-rows: 100%;
  }
}

.view {
  display: flex;
  flex-direction: column;
  justify-content: center;
  max-width: 27rem;
  height: 100%;
  margin: 0 auto;
  padding: 2rem;
}

.fade-enter-active {
  transition: all 100ms ease-in-out;
}

.fade-leave-active  {
  transition: all 50ms ease-in-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
