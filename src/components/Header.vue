<template>
    <header class="app-header">
        <h1>Header</h1>
        <button>➤</button> <!-- Placeholder for the icon/button (using a right arrow) -->
    </header>
</template>

<script setup>
</script>

<style scoped>
.app-header {
    background-color: #2C3E50;
    /* Dark blue color matching the image */
    color: white;
    width: 100%;
    height: 60px;
    /* Approximate height based on the image */
    display: flex;
    align-items: center;
    padding: 0 20px;
    /* Adds some padding for spacing */
    box-sizing: border-box;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
}

.app-header h1 {
    margin: 0;
    /* Remove default margin */
    font-size: 24px;
    /* Adjust font size to match the image */
}

.app-header button {
    margin-left: auto;
    /* Pushes the button to the right */
    background: none;
    border: none;
    color: white;
    cursor: pointer;
    font-size: 20px;
    padding: 5px;
    /* Small padding for clickable area */
}
</style>