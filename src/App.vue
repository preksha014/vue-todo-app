<script setup>
import { ref } from 'vue';
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Navbar from './components/Navbar.vue'

const activeTab = ref('Home');
const tabMap = {
    Home: Home,
    About: About,
    Contact: Contact
};

</script>



<template>
  <div id="app">
    <Header />
    <main>
      <keep-alive>
        <component :is="tabMap[activeTab]" />
      </keep-alive>
    </main>
    <Navbar :active-tab="activeTab" @update-tab="activeTab = $event" />
  </div>
</template>

<style>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: var(--color-background);
  color: var(--color-text);
  transition: color 0.5s, background-color 0.5s;
  width: 100%;
  position: relative;
}

main {
  flex: 1;
  width: 100%;
  display: flex;
  justify-content: center;
  box-sizing: border-box;
  background-color: var(--color-background);
  margin: 60px 0;
  padding: 1rem;
  padding-bottom: 80px;
}

@media (max-width: 768px) {
  main {
    padding: 1rem;
  }
}
</style>
