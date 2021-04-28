<template>
  <article class="home">
    <img class="logo" alt="Mucho logo" src="../assets/logo.svg">
    <p style="text-align: left;">Para Mayo lo sacamos. Prometido.🤞
    <br/>Si quieres que te avisemos, <strong>déjanos un email:</strong></p>
    <form name="contact" method="POST" data-netlify="true"
      data-netlify-honeypot="bot-field">
      <input type="hidden" name="form-name" value="contact">
      <input type="email" name="email" placeholder="micorreo@ejemplo.com" required/>
      <textarea name="message" placeholder="Mi mensaje (opcional)"></textarea>
      <button type="submit">Avísame</button>
    </form>
    <a href="mailto:info@revistamucho.com">info@revistamucho.com</a>
  </article>
</template>

<style lang="scss">
.logo {
  max-height: 42vh;
  margin-left: -6vh;
  margin-bottom: 3vh;
}

a {
  color: #a2a2a2;
  font-size: 0.7rem;
  margin-bottom: 1rem;
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
  margin-bottom: 1rem;
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
  font-family: Helvetica, sans-serif;
  -webkit-appearance: none;
  background: rgba(black, 0.1);
  border-bottom: 2px white solid;
}

</style>
