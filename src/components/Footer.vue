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
    background-color: var(--color-background-soft);
    box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.1);
    height: 60px;
    display: flex;
    align-items: center;
    z-index: 1000;
    color: var(--color-text);
    backdrop-filter: blur(10px);
}

.app-footer :deep(nav) {
    width: 100%;
    padding: 0 20px;
    display: flex;
    justify-content: center;
}

.app-footer :deep(.navbar ul) {
    display: flex;
    gap: 1rem;
    margin: 0;
    padding: 0;
}

.app-footer :deep(.navbar button) {
    background: none;
    border: none;
    color: var(--color-text);
    font-size: 0.9rem;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.app-footer :deep(.navbar button:hover) {
    background-color: var(--color-background-mute);
}

.app-footer :deep(.navbar button.active) {
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    color: var(--color-background);
}
</style>