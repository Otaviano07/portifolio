<script setup>
import { profile } from '../data';
</script>

<template>
  <section id="contact" class="contact">
    <h2>Contato</h2>
    <div class="contact-card">
      <p>Estou sempre aberto a novos projetos, colaborações e oportunidades na área de tecnologia e gestão.</p>
      <div class="email-wrapper">
        <a :href="'mailto:' + profile.contact.email" class="email-link">
          <span class="icon">✉</span>
          {{ profile.contact.email }}
        </a>
      </div>
      <p class="cta-text">Sinta-se à vontade para me enviar um e-mail!</p>
    </div>
  </section>
</template>

<style scoped>
.contact {
  text-align: center;
}

.contact-card {
  background-color: var(--card-bg);
  padding: 3rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  max-width: 600px;
  margin: 0 auto;
}

.contact-card p {
  color: var(--text-secondary);
  margin-bottom: 2rem;
  font-size: 1.1rem;
}

.email-wrapper {
  margin-bottom: 2rem;
}

.email-link {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 1.5rem;
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.3s, color 0.3s;
}

.email-link:hover {
  color: var(--text-primary);
  transform: scale(1.05);
}

.icon {
  font-size: 1.8rem;
}

.cta-text {
  font-size: 0.9rem !important;
  opacity: 0.7;
  margin-bottom: 0 !important;
}

@media (max-width: 600px) {
  .email-link {
    font-size: 1.1rem;
  }
}
</style>
