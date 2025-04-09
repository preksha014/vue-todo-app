<template>
    <div class="contact-container">
        <h1 class="contact-title">Contact Us</h1>
        <p class="contact-description">If you have any questions or comments, please feel free to reach out to us!</p>
        
        <form class="contact-form" @submit.prevent="handleSubmit">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" v-model="formData.name" required>
            </div>
            
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="formData.email" required>
            </div>
            
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" v-model="formData.message" rows="5" required></textarea>
            </div>
            
            <button type="submit" class="submit-button">Send Message</button>
        </form>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const formData = ref({
    name: '',
    email: '',
    message: ''
});

const handleSubmit = () => {
    // Here you would typically handle the form submission
    console.log('Form submitted:', formData.value);
    // Reset form after submission
    formData.value = {
        name: '',
        email: '',
        message: ''
    };
};
</script>

<style scoped>
.contact-container {
    max-width: 800px;
    margin: 2rem auto;
    padding: 2rem;
    background-color: var(--color-background-soft);
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.contact-title {
    color: var(--color-heading);
    font-size: 2rem;
    margin-bottom: 1rem;
    text-align: center;
    font-weight: 600;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent
}

.contact-description {
    text-align: center;
    margin-bottom: 2.5rem;
    color: var(--color-text);
    font-size: 1.1rem;
    line-height: 1.6
}

.contact-form {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.form-group label {
    color: var(--color-text);
    font-weight: 500;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 0.75rem 1rem;
    border: 2px solid var(--color-border);
    border-radius: 8px;
    background-color: var(--color-background);
    color: var(--color-text);
    font-size: 1rem;
    transition: all 0.3s ease;
    outline: none
}

.form-group input:focus,
.form-group textarea:focus {
    border-color: var(--color-heading);
    box-shadow: 0 0 0 3px rgba(var(--color-heading-rgb), 0.1)
}

.submit-button {
    width: 100%;
    padding: 0.75rem;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    color: var(--color-background);
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1)
}

.submit-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15)
}
</style>