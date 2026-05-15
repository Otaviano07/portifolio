<script setup>
import { profile } from '../data';

const skillCategories = [
  { title: 'Linguagens', items: profile.skills.languages },
  { title: 'Tecnologias & Interesses', items: profile.skills.interests },
  { title: 'Gestão & Soft Skills', items: profile.skills.management }
];
</script>

<template>
  <section id="skills" class="skills">
    <h2>Habilidades</h2>
    <div class="skills-container">
      <div v-for="category in skillCategories" :key="category.title" class="skill-category">
        <h3>{{ category.title }}</h3>
        <div class="skill-tags">
          <span v-for="skill in category.items" :key="skill" class="skill-tag">
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.skill-category {
  background-color: var(--card-bg);
  padding: 2rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: transform 0.3s;
}

.skill-category:hover {
  transform: translateY(-5px);
  border-color: rgba(56, 189, 248, 0.3);
}

.skill-category h3 {
  margin-bottom: 1.5rem;
  color: var(--accent-color);
  font-size: 1.2rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  padding-bottom: 0.5rem;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
}

.skill-tag {
  background-color: rgba(15, 23, 42, 0.5);
  color: var(--text-primary);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
  transition: all 0.3s;
}

.skill-tag:hover {
  background-color: var(--primary-color);
  border-color: var(--accent-color);
}

@media (max-width: 600px) {
  .skills-container {
    grid-template-columns: 1fr;
  }
}
</style>
