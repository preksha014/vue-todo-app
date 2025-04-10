<template>
    <nav class="navbar">
        <div class="nav-links">
            <router-link to="/" class="navbar-link" active-class="active">Home</router-link>
            <router-link to="/about" class="navbar-link" active-class="active">About</router-link>
            <router-link to="/contact" class="navbar-link" active-class="active">Contact</router-link>
        </div>
    </nav>
</template>

<script setup>
// defineProps({
//     activeTab: {
//         type: String,
//         required: true
//     }
// });

// defineEmits(['update-tab']);
</script>

<style scoped>
.navbar {
    width: 100%;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 20px;
    background-color: var(--color-background-soft);
    box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(10px);
}

.nav-links {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
}

.navbar-link {
    position: relative;
    color: var(--color-text);
    font-size: 1rem;
    font-weight: 500;
    padding: 0.6rem 1.2rem;
    border-radius: 8px;
    text-decoration: none;
    transition: all 0.3s ease;
    background: none;
    border: none;
    cursor: pointer;
    color: var(--color-text);
    font-size: 0.9rem;
    border-radius: 4px;
    transition: all 0.3s ease;
}

.navbar-link:hover {
    background-color: var(--color-background-mute);
    transform: translateY(-2px);
}

.navbar-link.active {
    background: none;
    color: var(--color-heading);
    font-weight: 600;
    box-shadow: none;
}

.navbar-link.active::after {
    width: 70%;
}

.navbar-link::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 50%;
    width: 0;
    height: 2px;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    transition: all 0.3s ease;
    transform: translateX(-50%);
}

.navbar-link:hover::after {
    width: 70%;
}

</style>