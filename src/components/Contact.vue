<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')

const submitForm = () => {
  alert(`Thank you, ${name.value}! Your message has been sent.`)
  name.value = ''
  email.value = ''
  message.value = ''
}
</script>

<template>
  <section id="contact" class="contact-section">
    <h2>Contact Me</h2>
    <div class="contact-container">
      <form @submit.prevent="submitForm" class="contact-form">
        <input type="text" v-model="name" placeholder="Your Name" required />
        <input type="email" v-model="email" placeholder="Your Email" required />
        <textarea v-model="message" placeholder="Your Message" rows="5" required></textarea>
        <button type="submit" class="btn-primary">Send Message</button>
      </form>

      <div class="contact-info">
        <h3>Get in Touch</h3>
        <p>Email: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
        <p>Phone: <a href="tel:+1234567890">+123 456 7890</a></p>
        <div class="social-links">
          <a href="#" target="_blank">LinkedIn</a>
          <a href="#" target="_blank">GitHub</a>
          <a href="#" target="_blank">Twitter</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  padding: 80px 20px;
  background: #f3f4f6;
  text-align: center;
}

.contact-section h2 {
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #1f2937;
}

.contact-container {
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
  justify-content: center;
}

.contact-form {
  background: white;
  color: white;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.08);
  flex: 1 1 300px;
  max-width: 400px;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 12px 15px;
  margin-bottom: 15px;
  border-radius: 8px;
  border: 1px solid #d1d5db;
  font-size: 1rem;
}

.contact-form button {
  background:black;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.contact-form button:hover {
  background: gray;
}

.contact-info {
  flex: 1 1 300px;
  max-width: 400px;
  text-align: left;
}

.contact-info h3 {
  font-size: 1.8rem;
  margin-bottom: 15px;
}

.contact-info p {
  font-size: 1rem;
  margin-bottom: 10px;
  color: #4b5563;
}

.social-links a {
  display: inline-block;
  margin-right: 15px;
  color: black;
  text-decoration: none;
  font-weight: bold;
}

.social-links a:hover {
  text-decoration: underline;
}
.p{
    color: black;
}
</style>
