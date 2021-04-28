<template>
  <article class="home">
    <img class="logo" alt="Mucho logo" src="../assets/logo.svg">
    <p>Para Mayo lo sacamos. Prometido.🤞
    <br/>Si quieres que te avisemos, <strong>apunta tu email:</strong></p>
    <form name="contact" method="POST" data-netlify="true"
      data-netlify-honeypot="bot-field">
      <input type="hidden" name="form-name" value="contact">
      <input type="email" name="email" placeholder="micorreo@ejemplo.com" />
      <label>Mensaje (opcional): <textarea name="message" placeholder="Mi mensaje"></textarea></label>
      <button type="submit">Avísame</button>
    </form>
  </article>
</template>

<style lang="scss">
.logo {
  max-height: 45vh;
}

.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  max-width: 23rem;
  height: 100%;
  margin: 0 auto;
  padding: 0 1rem;
}

form {
  width: 100%;
  margin: 0 auto;
}

label {
  display: block;
  width: 100%;
  text-align: center;
}

button {
  width: 100%;
  padding: 1rem;
  border-radius: 5px;
  border: none;
  background: #e6ad40;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  transition: all 150ms ease-in-out;

  &:hover {
    color: #e6ad40;
    background: black;
  }
}

input[type="email"],
textarea {
  width: 100%;
  display: block;
  margin: 1rem auto;
  padding: 1rem;
  border: none;
  color: white;
  -webkit-appearance: none;
  background: rgba(black, 0.1);
  border-bottom: 2px white solid;
}

</style>
