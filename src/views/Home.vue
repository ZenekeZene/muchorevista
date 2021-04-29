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
          "form-name": "contact",
          "subject": "¿Cuándo lo sacáis?",
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
<style lang="scss" scoped>
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
  height: 100%;
}
</style>
