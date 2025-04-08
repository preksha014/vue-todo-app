<template>
    <div class="todo-form">
        <h1>Todo Form</h1>
        <form @submit.prevent="addTodo">
            <div class="input-container">
                <input
                    type="text"
                    id="todo"
                    name="todo"
                    v-model.trim="todo"
                    placeholder="Enter Todo here"
                    required
                />
                <button type="submit" class="add-button">+</button>
            </div>
        </form>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const todo = ref('')

const addTodo = () => {
    if (todo.value) {
        console.log('Todo added:', todo.value)
        todo.value = '' // Clear the input after adding
    }
}
</script>

<style scoped>
.todo-form {
    padding: 1rem;
    width: 100%;
}

.todo-form h1 {
    color: var(--color-heading);
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
}

.input-container {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 2rem;
    background: var(--color-background);
    padding: 0.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
}

input {
    flex: 1;
    padding: 12px 16px;
    font-size: 1rem;
    border: 1px solid var(--color-border);
    border-radius: 6px;
    background-color: var(--color-background);
    color: var(--color-text);
    transition: all 0.3s ease;
}

input:focus {
    outline: none;
    border-color: var(--vt-c-indigo);
    box-shadow: 0 0 0 2px rgba(44, 62, 80, 0.1);
}

input::placeholder {
    color: var(--color-text-light-2);
}

.add-button {
    background-color: var(--vt-c-indigo);
    color: var(--vt-c-white);
    border: none;
    border-radius: 8px;
    width: 40px;
    height: 40px;
    font-size: 1.5rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.add-button:hover {
    background-color: var(--vt-c-indigo);
    transform: translateY(-1px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

@media (max-width: 768px) {
    .todo-form {
        padding: 0.5rem;
    }
    
    .input-container {
        padding: 0.25rem;
    }
    
    input {
        padding: 10px 14px;
    }
    
    .add-button {
        width: 36px;
        height: 36px;
        font-size: 1.25rem;
    }
}
</style>