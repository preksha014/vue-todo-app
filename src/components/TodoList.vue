<template>
    <div class="todo-list">
        <div v-for="(todo, index) in todos" :key="index" class="todo-item">
            <input type="checkbox" v-model="todo.completed" />
            <span :class="{ completed: todo.completed }">{{ todo.text }}</span>
            <button class="edit-button" @click="editTodo(index)">
                <span role="img" aria-label="edit">✏️</span>
            </button>
            <button class="delete-button" @click="deleteTodo(index)">
                <span role="img" aria-label="delete">🗑️</span>
            </button>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const todos = ref([
    { text: 'Study', completed: false },
    { text: 'Playing', completed: false },
])

const editTodo = (index) => {
    console.log('Edit todo:', todos.value[index].text)
}

const deleteTodo = (index) => {
    todos.value.splice(index, 1)
    console.log('Todo deleted')
}
</script>

<style scoped>
.todo-list {
    width: 100%;
    margin: 0 auto;
    background-color: transparent;
    padding: 1rem;
}

.todo-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 1rem;
    background-color: var(--color-background);
    border-radius: 8px;
    margin-bottom: 1rem;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
    border: 1px solid var(--color-border);
}

.todo-item:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    border-color: var(--color-border-hover);
}

input[type="checkbox"] {
    margin: 0;
    cursor: pointer;
    width: 22px;
    height: 22px;
    border: 2px solid var(--vt-c-indigo);
    border-radius: 6px;
    appearance: none;
    -webkit-appearance: none;
    position: relative;
    background-color: var(--color-background);
    transition: all 0.2s ease;
}

input[type="checkbox"]:checked {
    background-color: var(--vt-c-indigo);
    border-color: var(--vt-c-indigo);
}

input[type="checkbox"]:checked::after {
    content: "✓";
    position: absolute;
    color: var(--vt-c-white);
    font-size: 14px;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}

input[type="checkbox"]:hover {
    border-color: var(--vt-c-indigo);
    box-shadow: 0 0 0 2px rgba(44, 62, 80, 0.1);
}

span {
    flex: 1;
    font-size: 1rem;
    color: var(--color-text);
    transition: all 0.3s ease;
}

.completed {
    text-decoration: line-through;
    opacity: 0.6;
    color: var(--color-text-light-2);
}

.edit-button, .delete-button {
    border: none;
    border-radius: 8px;
    width: 32px;
    height: 32px;
    font-size: 16px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    background-color: var(--color-background-soft);
    color: var(--color-text);
}

.edit-button:hover, .delete-button:hover {
    background-color: var(--color-background-mute);
    transform: translateY(-1px);
}
</style>