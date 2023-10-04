<template>
  <section class="portfolio-home">
    <header class="portfolio-header">
      <h1 style="color: #32429d;">Jake Pyrczak</h1>
      <p>IT Student and Developer</p>
    </header>

    <section class="portfolio-intro">
      <p>
        Hello! I'm Jake, a passionate IT student in my final year of university. I love different kinds of programming. Check out my projects below!
      </p>
    </section>

    <section class="portfolio-projects">
      <h2>My Projects</h2>
      <div class="projects-grid">
        <div class="project-card" v-for="project in projects" :key="project.id">
          <img :src="project.image" :alt="project.name" class="project-image"/>
          <h3>{{ project.name }}</h3>
          <p style="margin-left:15px; margin-right:10px; text-align: center;">{{ project.description }}</p>
        </div>
      </div>
    </section>

    <footer class="portfolio-footer">
      <p>Thank you for visiting! Let's <a href="mailto:jpyrczak@deakin.edu.au">connect</a></p>
    </footer>
  </section>
</template>

<script setup>
import { ref } from 'vue';

import { projects } from '/src/data/project_data.json';
const project = ref(projects);

</script>

<style scoped>
.portfolio-home {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.portfolio-header {
  text-align: center;
  margin-bottom: 50px;
  
}

.portfolio-header h1 {
  font-size: 2.5em;
  margin-bottom: 10px;
}

.portfolio-intro {
  text-align: center;
  margin-bottom: 80px;
}

.portfolio-projects {
  margin-bottom: 50px;
}

.portfolio-projects h2 {
  color: #32429d;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
}

.project-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  overflow: hidden;
}

.project-card img {
  width: 100%;
  height: auto;
}

.project-card h3 {
  text-align: center;
  padding: 10px 0;
}

.portfolio-footer {
  text-align: center;
}

.project-image {
  max-width: 400px; /* Set the maximum width you want for the image */
  max-height: 400px; /* Set the maximum height you want for the image */
  width: auto; /* Maintain the aspect ratio of the image */
  height: auto; /* Maintain the aspect ratio of the image */
}
</style>