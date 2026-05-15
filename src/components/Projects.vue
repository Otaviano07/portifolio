<script setup>
import { profile } from '../data';
</script>

<template>
  <section id="projects" class="projects">
    <h2>Meus Projetos</h2>
    <div class="projects-grid">
      <div v-for="project in profile.projects" :key="project.title" class="project-card">
        <div class="project-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <div class="project-tags">
            <span v-for="tag in project.tags" :key="tag" class="project-tag">{{ tag }}</span>
          </div>
          <a :href="project.link" target="_blank" rel="noopener noreferrer" class="project-link">
            Visitar Site <span>→</span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.project-card {
  background-color: var(--card-bg);
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-10px);
  border-color: var(--accent-color);
  box-shadow: 0 20px 40px -20px rgba(0, 0, 0, 0.5);
}

.project-content {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  height: 100%;
}

h3 {
  color: var(--text-primary);
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

p {
  color: var(--text-secondary);
  margin-bottom: 1.5rem;
  font-size: 1rem;
  flex-grow: 1;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.project-tag {
  background-color: rgba(37, 99, 235, 0.1);
  color: var(--accent-color);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  font-size: 0.8rem;
  font-weight: 600;
}

.project-link {
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 700;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  transition: gap 0.3s;
}

.project-link span {
  transition: transform 0.3s;
}

.project-link:hover {
  text-decoration: underline;
}

.project-link:hover span {
  transform: translateX(5px);
}

@media (max-width: 600px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>
