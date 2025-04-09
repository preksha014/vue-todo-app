<template>
    <div class="about-container">
        <h1 class="about-title">About Us</h1>
        <div class="about-content">
            <p>We are a team of passionate developers dedicated to creating amazing applications.</p>
            <p>Our mission is to provide the best user experience through innovative solutions.</p>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.about-container {
    max-width: 800px;
    margin: 2rem auto;
    padding: 2rem;
    background-color: var(--color-background-soft);
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.about-title {
    color: var(--color-heading);
    font-size: 2rem;
    margin-bottom: 1.5rem;
    text-align: center;
}

.about-content {
    color: var(--color-text);
    line-height: 1.6;
}

.about-content {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.about-content p {
    margin: 0;
    line-height: 1.8;
    color: var(--color-text);
    font-size: 1.1rem;
    padding: 1rem;
    background-color: var(--color-background-mute);
    border-radius: 8px;
    transition: transform 0.3s ease;
}

.about-content p:hover {
    transform: translateY(-2px);
}
</style>