<template>
    <div class="filter-container">
        <form>
            <label for="filter">Filter:</label>
            <select id="filter" name="filter" v-model="selectedFilter">
                <option value="all">All</option>
                <option value="completed">Completed</option>
                <option value="remaining">Remaining</option>
            </select>
        </form>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const selectedFilter = ref('all') // Default value set to 'all'
</script>

<style scoped>
.filter-container {
    background-color: var(--color-background-soft);
    padding: 1rem;
    border-radius: 8px;
    margin: 1.5rem 0;
    width: 100%;
}

form {
    display: flex;
    align-items: center;
    gap: 1rem;
}

label {
    color: var(--color-text);
    font-weight: 600;
    font-size: 1rem;
    min-width: 60px;
}

select {
    padding: 0.5rem 2rem 0.5rem 1rem;
    font-size: 1rem;
    border: 1px solid var(--color-border);
    border-radius: 4px;
    background-color: var(--color-background);
    appearance: none;
    cursor: pointer;
    flex: 1;
    color: var(--color-text);
    transition: border-color 0.3s, box-shadow 0.3s;
}

form {
    position: relative;
}

form::after {
    content: '▼';
    position: absolute;
    right: 1rem;
    top: 50%;
    transform: translateY(-50%);
    pointer-events: none;
    color: var(--color-text);
    font-size: 0.8rem;
}

select::-moz-focus-inner {
    border: 0;
}

option {
    background-color: var(--color-background);
    color: var(--color-text);
    padding: 0.5rem;
}

select:focus {
    outline: none;
    border-color: var(--color-border-hover);
    box-shadow: 0 0 0 2px rgba(44, 62, 80, 0.1);
}

select:hover {
    border-color: var(--color-border-hover);
}

@media (max-width: 768px) {
    form {
        flex-direction: column;
        align-items: stretch;
    }

    label {
        margin-bottom: 0.5rem;
    }
}
</style>