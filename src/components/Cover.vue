<template>
  <article class="cover">
    <img src="/img/cover.png" alt="Mockup de la revista" />
  </article>
</template>
<style scoped lang="scss">
.cover {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background-color: #aad6d5;

  img {
    width: auto;
    height: 70%;
    filter: drop-shadow(5px 5px 5px #222);
    animation: shit 2s ease-in-out infinite;
    transition: all 50ms ease-in-out;
  }

  &:hover img {
    transform: scale(1.1);
  }
}

@keyframes shit {
  0% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-5px);
  }

  100% {
    transform: translateY(0);
  }
}
</style>
