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
    margin: 0;
    padding: 1.8rem;
    background-color: var(--color-background-soft);
    border-radius: 16px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
    margin-top: 80px; /* Account for header height */
    margin-bottom: 80px; /* Account for footer height */
    border: 1px solid var(--color-border);
}

.contact-title {
    color: var(--color-heading);
    font-size: 1.5rem;
    margin-bottom: 1rem;
    text-align: center;
    font-weight: 600;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.contact-description {
    text-align: center;
    margin-bottom: 1rem;
    color: var(--color-text);
    font-size: 1.1rem;
    line-height: 1.6;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

.contact-form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
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
    padding: 0.85rem 1.2rem;
    border: 2px solid var(--color-border);
    border-radius: 12px;
    background-color: var(--color-background);
    color: var(--color-text);
    font-size: 1rem;
    transition: all 0.3s ease;
    outline: none;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

.form-group input:focus,
.form-group textarea:focus {
    border-color: var(--color-heading);
    box-shadow: 0 0 0 3px rgba(44, 62, 80, 0.1);
    transform: translateY(-2px);
}

.submit-button {
    width: 100%;
    padding: 0.85rem;
    background: linear-gradient(45deg, var(--color-heading), var(--color-text));
    color: var(--color-background);
    border: none;
    border-radius: 12px;
    font-size: 1.1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    letter-spacing: 0.5px;
}

.submit-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
}
</style>