<script setup>
import { ref } from 'vue'

const name = ref('');
const email = ref('');
const message = ref('');
</script>

<template>
  <section id="contact">
    <h1>Contact</h1>
    <form>
      <label>Name:</label>
      <input v-model="name" type="text" />

      <label>Email:</label>
      <input v-model="email" type="email" />

      <label>Message:</label>
      <textarea v-model="message"></textarea>

      <button type="submit">Submit</button>
    </form>
  </section>
</template>

<style scoped>
section {
  min-height: 90vh;
  margin: 0;
  background-color: #a2d1f0;
  color: white;
  font-size: 30px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  opacity: 0;
  animation: fadeIn 1s forwards;
}

h1 {
  font-size: 100px;
  font-weight: bold;
  margin-bottom: 50px;
}

form {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

label {
  font-size: 35px;
  margin-bottom: 0;
}

input, textarea {
  padding: 12px;
  margin-bottom: 25px;
  border-radius: 5px;
  border: 1px solid #ddd;
  width: 600px;
  background-color: rgb(105, 105, 105);
}

button {
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 12px 15px;
  font-size: 20px;
  font-weight: 500;
  background-color: #16a085;
  cursor: pointer;
  margin: 20px 0;
  margin-bottom: 100px;
  transition: border-color 0.25s;
}

button:hover {
  background-color: #1abc9c;
}

@keyframes fadeIn {
  to {
    opacity: 1;
  }
}
</style>