<template>
  <div class="contact-form">
    <h2>Contact Form</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" />
      </div>
      <div class="form-group">
        <label for="phone">Phone:</label>
        <input type="tel" id="phone" v-model="phone" />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" rows="4" v-model="message"></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      phone: '',
      message: ''
    };
  },
  methods: {
    async submitForm() {
      // Kirim data formulir ke Formspree atau lakukan console.log
      const formData = {
        name: this.name,
        email: this.email,
        phone: this.phone,
        message: this.message
      };
      
      console.log(formData);

      // Atau gunakan Formspree untuk mengirim email
      // Ubah "YOUR_FORMSPREE_ENDPOINT" dengan endpoint Formspree Anda
      // await fetch('YOUR_FORMSPREE_ENDPOINT', {
      //   method: 'POST',
      //   body: JSON.stringify(formData)
      // });

      // Reset nilai input setelah mengirim formulir
      this.name = '';
      this.email = '';
      this.phone = '';
      this.message = '';
    }
  }
};
</script>

<style>
.contact-form {
  margin-top: 20px;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 10px;
}

label {
  display: block;
}

input,
textarea {
  width: 100%;
  padding: 5px;
}
</style>
