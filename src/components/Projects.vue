<script setup>
const projects = [
  {
    title: "Retail POS System",
    description: "A modern POS with inventory tracking, sales analytics, and receipt management.",
    image: "/projects/pos.jpg",
    link: "#"
  },
  {
    title: "Student Enquiry Platform",
    description: "A web app for students and professors to manage enquiries and feedback.",
    image: "/projects/enquiry.jpg",
    link: "#"
  },
  {
    title: "Freelance Marketplace",
    description: "A niche marketplace connecting African software engineers with global clients.",
    image: "/projects/marketplace.jpg",
    link: "#"
  }
]
</script>

<template>
  <section id="projects" class="projects-section">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div v-for="(project, index) in projects" :key="index" class="project-card">
        <img :src="project.image" :alt="project.title" />
        <div class="card-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" target="_blank" class="btn-secondary">View Project</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects-section {
  padding: 80px 20px;
  background: #f9fafb;
  text-align: center;
}

.projects-section h2 {
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #1f2937;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
}

.project-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(0,0,0,0.08);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.12);
}

.project-card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

.card-content {
  padding: 20px;
  text-align: left;
}

.card-content h3 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: #111827;
}

.card-content p {
  font-size: 1rem;
  color: #4b5563;
  margin-bottom: 15px;
}

.btn-secondary {
  display: inline-block;
  padding: 10px 18px;
  background: black;
  color: white;
  border-radius: 8px;
  text-decoration: none;
  transition: background 0.3s ease;
}

.btn-secondary:hover {
  background: gray;
}
</style>
