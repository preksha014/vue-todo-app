<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue';

// const activeTab = ref('Home');
// const tabMap = {
//     Home: Home,
//     About: About,
//     Contact: Contact
// };

</script>



<template>
  <div id="app">
    <Header />
    <main>
      <router-view></router-view>
    </main>
    <Footer />
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
  padding: 0;
  min-height: calc(100vh - 120px);
}

@media (max-width: 768px) {
  main {
    padding: 0 0.5rem;
  }
}
</style>
