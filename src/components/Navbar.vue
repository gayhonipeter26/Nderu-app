<template>
  <nav class="navbar">
    <div class="logo">MyPortfolio</div>
    <ul class="nav-links">
      <li><a href="#hero">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  background: #222;
  color: white;
  position: sticky;
  top: 0;
  z-index: 1000;
}
.logo {
  font-size: 1.5rem;
  font-weight: bold;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 20px;
}
.nav-links a {
  text-decoration: none;
  color: white;
  transition: 0.3s;
}
.nav-links a:hover {
  color: #00adb5;
}
</style>
