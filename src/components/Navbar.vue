<template>
    <nav class="navbar">
        <ul>
            <button @click="$emit('update-tab', 'Home')" :class="{ active: activeTab === 'Home' }">Home</button>
            <button @click="$emit('update-tab', 'About')" :class="{ active: activeTab === 'About' }">About</button>
            <button @click="$emit('update-tab', 'Contact')"
                :class="{ active: activeTab === 'Contact' }">Contact</button>
        </ul>
    </nav>
</template>

<script setup>
defineProps({
    activeTab: {
        type: String,
        required: true
    }
});

defineEmits(['update-tab']);
</script>

<style scoped>
.navbar {
    width: 100%;
    height: 60px;
    display: flex;
    align-items: center;
    padding: 0 20px;
    background-color: var(--color-background-soft);
    box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.1);
    position: fixed;
    bottom: 0;
    left: 0;
    z-index: 1000;
    backdrop-filter: blur(10px);
}

.navbar ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    gap: 20px;
    width: 100%;
    justify-content: center;
}

button {
    background: none;
    border: none;
    padding: 0.5rem 1rem;
    margin: 0;
    cursor: pointer;
    color: var(--color-text);
    font-size: 0.9rem;
    border-radius: 4px;
    transition: all 0.3s ease;
}

button:hover {
    background-color: var(--color-background-mute);
}

button.active {
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    color: var(--color-background);
    font-weight: 500;
}
</style>