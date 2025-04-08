<template>
    <footer class="app-footer">
        <Navbar />
    </footer>
</template>

<script setup>
import Navbar from './Navbar.vue'
</script>

<style scoped>
.app-footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #2C3E50;
    box-shadow: 0 -2px 5px rgba(0, 0, 0, 0.1);
}

h1 {
    margin: 0;
    padding: 10px;
    background-color: #F5F5DC;
    /* Light cream color from the image's top edge */
}
</style>