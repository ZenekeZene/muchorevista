<template>
  <article class="home">
    <img class="logo" alt="Mucho logo" src="../assets/logo.svg">
    <p>Se que tienes ganas.
      <br/>Nosotros también.
      <br/>Para Mayo lo sacamos.
      <br/>Prometido.🤞
    </p>
    <form name="contact" method="POST" netlify>
      <label>Your Email: <input type="email" name="email" /></label>
      <label>Message: <textarea name="message"></textarea></label>
      <button type="submit">Send</button>
    </form>
  </article>
</template>

<style lang="scss">
.logo {
  max-height: 75vh;
  margin-left: -10vw;
}
</style>
