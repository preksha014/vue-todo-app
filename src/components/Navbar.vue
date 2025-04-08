<template>
    <nav class="navbar">
        <ul>
            <li><a href="#home" class="active">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</template>

<script setup>
</script>

<style scoped>
.navbar {
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
    padding: 0 20px;
    box-sizing: border-box;
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

.navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 16px;
    padding: 5px 10px;
    transition: all 0.3s ease;
}

.navbar ul li a:hover {
    color: #E57373;
}

.navbar ul li a.active {
    background-color: #E57373;
    color: white;
    border-radius: 4px;
}
</style>