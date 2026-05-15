<script setup>
import { profile } from '../data';
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="hashtags">
        <span v-for="tag in profile.hashtags" :key="tag" class="hashtag">{{ tag }}</span>
      </div>
      <div class="divider"></div>
      <p>&copy; {{ currentYear }} - {{ profile.name }}. Todos os direitos reservados.</p>
      <p class="tagline">Construindo soluções inovadoras com tecnologia e gestão.</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #020617;
  padding: 4rem 1rem;
  text-align: center;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.footer-content {
  max-width: 1000px;
  margin: 0 auto;
}

.hashtags {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 2rem;
}

.hashtag {
  color: var(--accent-color);
  font-size: 0.85rem;
  opacity: 0.8;
}

.divider {
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(255, 255, 255, 0.1), transparent);
  margin: 2rem 0;
}

p {
  color: var(--text-secondary);
  font-size: 0.95rem;
}

.tagline {
  margin-top: 0.5rem;
  font-size: 0.85rem;
  opacity: 0.6;
}
</style>
