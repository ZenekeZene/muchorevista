<template>
  <article class="home">
    <img class="logo" alt="Mucho logo" src="../assets/logo.svg">
    <p style="text-align: left;">Para Mayo lo sacamos. Prometido.🤞
    <br/>Si quieres que te avisemos, <strong>déjanos un email:</strong></p>
    <form
      name="contact"
      method="post"
      data-netlify="true"
      data-netlify-honeypot="bot-field"
      @submit.prevent="handleSubmit"
    >
      <input
        type="hidden"
        name="form-name"
        value="contact"
      />
      <input
        type="email"
        name="email"
        placeholder="micorreo@ejemplo.com"
        required
        @input="ev => form.email = ev.target.value"
      />
      <textarea
        name="message"
        placeholder="Mi mensaje (opcional)"
        @input="ev => form.message = ev.target.value"
      ></textarea>
      <button type="submit">Avísame</button>
    </form>
    <a href="mailto:info@revistamucho.com">info@revistamucho.com</a>
  </article>
</template>
<script>

export default {
  data () {
    return {
      form: {
        email: '',
        message: ''
      }
    }
  },
  methods: {
    encode (data) {
      return Object.keys(data)
        .map(
          key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join("&");
    },
    handleSubmit () {
      fetch("/", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body: this.encode({
          "form-name": "ask-question",
          ...this.form
        })
      })
      .then(() => {
        this.$router.push('thanks')
      })
      .catch(() => {
        this.$router.push('404')
      })
    }
  }
}
</script>
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
  height: 100%;
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
  max-width: 23rem;
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
