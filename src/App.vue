<template>
  <main id="app">
    <transition name="fade" mode="in-out">
      <router-view class="view" />
    </transition>
  </main>
</template>

<style lang="scss" scoped>
#app {
  position: relative;
  max-width: 23rem;
  height: 100%;
  margin: 0 auto;
  padding: 0 1rem;
  text-align: center;
}

.view {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
  width: 100%;
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
