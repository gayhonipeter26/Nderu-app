<script setup>
import { ref, onMounted } from 'vue'

const typedText = ref('')
const texts = ['Software Developer', 'Web Enthusiast', 'Problem Solver']
let index = 0
let charIndex = 0

const type = () => {
  if (charIndex < texts[index].length) {
    typedText.value += texts[index][charIndex]
    charIndex++
    setTimeout(type, 150)
  } else {
    setTimeout(erase, 1000)
  }
}

const erase = () => {
  if (charIndex > 0) {
    typedText.value = typedText.value.slice(0, charIndex - 1)
    charIndex--
    setTimeout(erase, 100)
  } else {
    index = (index + 1) % texts.length
    setTimeout(type, 500)
  }
}

onMounted(() => {
  type()
})
</script>

<template>
  <section class="hero">
    <div class="hero-content">
      <h1>Hello, I'm Nderu</h1>
      <h2>I am a <span class="typed">{{ typedText }}</span></h2>
      <p>Building modern web applications and crafting seamless user experiences.</p>
      <div class="hero-buttons">
        <a href="#projects" class="btn-primary">View Projects</a>
        <a href="#contact" class="btn-secondary">Contact Me</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  height: 100vh;
  background: linear-gradient(135deg,gray,black);
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
  padding: 0 20px;
}

.hero-content h1 {
  font-size: 3rem;
  margin-bottom: 15px;
  color: white;
}

.hero-content h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: white;
}

.typed {
  border-right: 2px solid white;
  padding-right: 5px;
}

.hero-content p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.hero-buttons a {
  text-decoration: none;
  padding: 12px 25px;
  margin: 5px;
  border-radius: 8px;
  font-weight: bold;
  transition: all 0.3s ease;
}

.btn-primary {
  background: white;
  color:gray;
}

.btn-primary:hover {
  background: #e0e7ff;
}

.btn-secondary {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.1);
}
</style>
