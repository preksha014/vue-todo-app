<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
</script>

<template>
  <Header />
  <main>
    <Home />
  </main>
  <Footer />
</template>

<style>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: var(--color-background);
  color: var(--color-text);
  transition: all 0.3s ease;
  width: 100%;
}

main {
  flex: 1;
  width: 100%;
  display: flex;
  justify-content: center;
  padding: 2rem;
  box-sizing: border-box;
  background-color: var(--color-background);
}

@media (max-width: 768px) {
  main {
    padding: 1rem;
  }
}
</style>
