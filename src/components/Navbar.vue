<template>
  <nav class="navbar">
    <div class="nav-content">
      <div class="logo">OR<span>S</span></div>
      <ul class="nav-links">
        <li><a href="#hero">Início</a></li>
        <li><a href="#about">Sobre</a></li>
        <li><a href="#skills">Habilidades</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  background-color: rgba(15, 23, 42, 0.9);
  backdrop-filter: blur(10px);
  z-index: 1000;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.nav-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: var(--text-primary);
  letter-spacing: 2px;
}

.logo span {
  color: var(--accent-color);
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links a {
  text-decoration: none;
  color: var(--text-secondary);
  font-weight: 500;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: var(--accent-color);
}

@media (max-width: 480px) {
  .nav-links {
    gap: 1rem;
    font-size: 0.9rem;
  }
}
</style>
