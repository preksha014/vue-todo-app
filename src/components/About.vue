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
    margin: 0 auto;
    padding: 2.5rem;
    background-color: var(--color-background-soft);
    border-radius: 16px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
    margin-top: 80px; /* Account for header height */
    margin-bottom: 80px; /* Account for footer height */
    border: 1px solid var(--color-border);
}

.about-title {
    color: var(--color-heading);
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    text-align: center;
    font-weight: 600;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.about-content {
    color: var(--color-text);
    line-height: 1.6;
}

.about-content {
    display: flex;
    flex-direction: column;
}

.about-content p {
    margin: 0;
    line-height: 1.8;
    color: var(--color-text);
    font-size: 1.1rem;
    padding: 0.5rem;
    transition: transform 0.3s ease;
}

.about-content p:hover {
    transform: translateY(-2px);
}
</style>