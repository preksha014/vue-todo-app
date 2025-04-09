<template>
    <header class="app-header">
        <h1>Todo App</h1>
        <button class="theme-toggle" title="Toggle theme">
            <span class="toggle-icon">🌙</span>
        </button>
    </header>
</template>

<script setup>
</script>

<style scoped>
.app-header {
    background-color: var(--color-background-soft);
    color: var(--color-heading);
    width: 100%;
    height: 60px;
    display: flex;
    align-items: center;
    padding: 0 20px;
    box-sizing: border-box;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(10px);
}

.app-header h1 {
    margin: 0;
    font-size: 24px;
    font-weight: 600;
    letter-spacing: 0.5px;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.theme-toggle {
    margin-left: auto;
    background: none;
    border: 2px solid var(--color-border);
    color: var(--color-text);
    cursor: pointer;
    width: 40px;
    height: 40px;
    padding: 0;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}

.theme-toggle:hover {
    background-color: var(--color-background-mute);
    transform: scale(1.05);
}

.toggle-icon {
    font-size: 18px;
    line-height: 1;
}
</style>