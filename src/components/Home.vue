<template>
    <div class="home-container">
        <div class="todo-section">
            <TodoForm />
            <FilterList />
            <TodoList />
        </div>
    </div>
</template>

<script setup>
import TodoForm from './TodoForm.vue'
import TodoList from './TodoList.vue'
import FilterList from './FilterList.vue'
</script>

<style scoped>
.home-container {
    min-height: calc(100vh - 120px);
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
    padding-top: 2rem;
    background-color: var(--color-background);
    display: flex;
    justify-content: center;
    align-items: flex-start;
}

.todo-section {
    width: 100%;
    background-color: var(--color-background-soft);
    border-radius: 12px;
    padding: 2rem;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(10px);
    max-width: 800px;
    background-color: var(--color-background-soft);
    border-radius: 12px;
    padding: 2rem;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
    transition: all 0.3s ease;
}

@media (min-width: 1024px) {
    .todo-section {
        padding: 2.5rem;
    }
}

@media (max-width: 768px) {
    .home-container {
        padding: 1rem;
        padding-top: calc(1rem + 60px);
    }

    .todo-section {
        padding: 1.5rem;
        border-radius: 8px;
    }
}
</style>