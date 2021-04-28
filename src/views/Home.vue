<template>
  <article class="home">
    <img class="logo" alt="Mucho logo" src="../assets/logo.svg">
    <p>Se que tienes ganas.
      <br/>Nosotros también.
      <br/>Para Mayo lo sacamos.
      <br/>Prometido.🤞
    </p>
    <form name="contact" method="POST" data-netlify="true">
      <p>
        <label>Your Name: <input type="text" name="name" /></label>
      </p>
      <p>
        <label>Your Email: <input type="email" name="email" /></label>
      </p>
      <p>
        <label>Your Role: <select name="role[]" multiple>
          <option value="leader">Leader</option>
          <option value="follower">Follower</option>
        </select></label>
      </p>
      <p>
        <label>Message: <textarea name="message"></textarea></label>
      </p>
      <p>
        <button type="submit">Send</button>
      </p>
    </form>
  </article>
</template>

<style lang="scss">
.logo {
  max-height: 75vh;
  margin-left: -10vw;
}
</style>
