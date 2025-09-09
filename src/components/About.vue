<script setup>
import profilePic from '../assets/profile.jpeg'
</script>

<template>
  <section id="about" class="about-section">
    <div class="about-container">
      <!-- Profile picture -->
      <div class="about-image">
        <img :src="profilePic" alt="Profile Picture" />
      </div>

      <!-- About text -->
      <div class="about-text">
        <h2>About Me</h2>
        <p>
          Hi! I’m a passionate software developer who builds modern web
          applications using Vue.js, JavaScript, and other cutting-edge
          technologies. I focus on creating clean, user-friendly, and
          high-performance solutions.
        </p>
        <p>
          I enjoy tackling challenging problems, learning new tools, and
          delivering products that make a real impact.
        </p>

        <a href="#projects" class="btn-primary">See My Projects</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 80px 20px;
  background: #f9f9f9;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.about-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  max-width: 1000px;
  margin: 0 auto;
  gap: 40px;
}

.about-image img {
  width: 220px;
  height: 220px;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.about-image img:hover {
  transform: scale(1.05);
}

.about-text {
  flex: 1;
  min-width: 280px;
}

.about-text h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: #333;
}

.about-text p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
  margin-bottom: 15px;
}

.btn-primary {
  display: inline-block;
  padding: 12px 25px;
  background-color:black;
  color: white;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  transition: background 0.3s ease;
}

.btn-primary:hover {
  background-color:black;
}
</style>
