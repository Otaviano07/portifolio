<script setup>
import { profile } from '../data';
</script>

<template>
  <section id="about" class="about">
    <h2>Sobre Mim</h2>
    <div class="about-grid">
      <div class="about-text">
        <p v-for="(paragraph, index) in profile.about.split('\n\n')" :key="index">
          {{ paragraph }}
        </p>
      </div>
      <div class="experience-card">
        <h3>Experiência de Destaque</h3>
        <p><strong>8+ Anos</strong> em Gestão de Estoque</p>
        <p>Setores Administrativo e Qualidade</p>
        <div class="highlight-box">
          Focado em Análise de Dados e Otimização de Processos.
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 3rem;
  align-items: start;
}

.about-text p {
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
  color: var(--text-secondary);
}

.experience-card {
  background-color: var(--card-bg);
  padding: 2rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  box-shadow: 0 10px 30px -15px rgba(0, 0, 0, 0.5);
}

.experience-card h3 {
  color: var(--accent-color);
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

.experience-card p {
  margin-bottom: 0.5rem;
}

.highlight-box {
  margin-top: 1.5rem;
  padding: 1rem;
  background-color: rgba(56, 189, 248, 0.1);
  border-left: 4px solid var(--accent-color);
  font-style: italic;
  font-size: 0.95rem;
}

@media (max-width: 850px) {
  .about-grid {
    grid-template-columns: 1fr;
  }
}
</style>
