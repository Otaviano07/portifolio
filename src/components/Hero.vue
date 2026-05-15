<script setup>
import { profile } from '../data';
</script>

<template>
  <section id="hero" class="hero">
    <div class="hero-content">
      <h1 class="fade-in">Olá, sou <span>{{ profile.name }}</span></h1>
      <p class="role">{{ profile.role }}</p>
      <p class="institution">{{ profile.institution }}</p>
      <div class="cta-buttons">
        <a href="#about" class="btn btn-primary">Conhecer mais</a>
        <a href="#skills" class="btn btn-secondary">Ver Habilidades</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: radial-gradient(circle at center, rgba(37, 99, 235, 0.1) 0%, transparent 70%);
}

h1 {
  font-size: 3.5rem;
  margin-bottom: 0.5rem;
}

h1 span {
  color: var(--accent-color);
}

.role {
  font-size: 1.5rem;
  color: var(--text-secondary);
  font-weight: 500;
  margin-bottom: 0.25rem;
}

.institution {
  font-size: 1.1rem;
  color: var(--text-secondary);
  margin-bottom: 2.5rem;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
}

.btn {
  padding: 0.8rem 2rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s;
}

.btn-primary {
  background-color: var(--primary-color);
  color: white;
}

.btn-primary:hover {
  background-color: var(--secondary-color);
  transform: translateY(-2px);
}

.btn-secondary {
  border: 1px solid var(--primary-color);
  color: var(--accent-color);
}

.btn-secondary:hover {
  background-color: rgba(37, 99, 235, 0.1);
  transform: translateY(-2px);
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.fade-in {
  animation: fadeIn 1s ease-out forwards;
}

@media (max-width: 768px) {
  h1 { font-size: 2.5rem; }
  .role { font-size: 1.2rem; }
  .cta-buttons { flex-direction: column; gap: 1rem; }
}
</style>
