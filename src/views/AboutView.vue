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
    
    <table v-if="submittedData.length > 0">
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
          <th>Phone</th>
          <th>Message</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(data, index) in submittedData" :key="index">
          <td>{{ data.name }}</td>
          <td>{{ data.email }}</td>
          <td>{{ data.phone }}</td>
          <td>{{ data.message }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      phone: '',
      message: '',
      submittedData: [] // Array untuk menyimpan data yang telah disubmit
    };
  },
  methods: {
    async submitForm() {
      const formData = {
        name: this.name,
        email: this.email,
        phone: this.phone,
        message: this.message
      };

      // Menambahkan data yang disubmit ke dalam array submittedData
      this.submittedData.push(formData);

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

table {
  width: 100%;
  border-collapse: collapse;
}

table th,
table td {
  padding: 8px;
  border: 1px solid #ccc;
}

table th {
  background-color: #f2f2f2;
}
</style>
