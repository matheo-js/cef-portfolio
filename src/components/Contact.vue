<script setup>

    const sendMail = () => {
        alert('merci pour votre message ! Je vous recontacterai dans les plus brefs délais.') 
    }

</script>

<template>

    <section id="contact">
        <div class="center contact-container">
            <p class="job-title">03 — Contact</p>
            <h2>Discutons de votre projet !</h2>

            <p>
               Vous avez un projet innovant, un besoin d'expertise Vue.js / Nuxt 3 ou souhaitez simplement échanger autour de l'architecture frontend ? Parlons-en !
            </p>
        
            <form @submit.prevent="sendMail()">

                <div class="name-container">
                    <div class="input-container">
                        <label for="firstname">prenom</label>
                        <input id="firstname" name="firstname" type="text" placeholder="Ex : Jhone" required> 
                    </div>

                    <div class="input-container">
                        <label for="lastname">nom</label>
                        <input id="lastname" name="lastname" type="text" placeholder="Ex : Doe" required> 
                    </div>
                </div>

                <div class="input-container">
                    <label for="email">email</label>
                    <input id="email" name="email" type="email" placeholder="test@gmail.com" required> 
                </div>

                <div class="input-container">
                    <label for="message">message</label>
                    <textarea id="message" name="message" placeholder="Ex : Bonjour, je souhaite vous contacter pour..." required></textarea> 
                </div>

                <button type="submit">Envoyer</button>

            </form>
        </div>
    </section>

</template>


<style scoped>

    .contact-container {
        padding: 3rem 1.5rem;
    }
    
    /* contact */

    .contact-container h2 {
        font-size: var(--text-xl);
        color: var(--color-primary);
        text-transform: uppercase;
        font-weight: bold;
        text-wrap: balance;
    }

    .contact-container p {
        color: var(--color-secondary);
        font-size: var(--text-base);
        line-height: 1.5;
        margin-top: 1rem;
        text-wrap: balance;

    }

    form {
        display: flex;
        flex-direction: column;
        gap: 1.6rem;
        margin-top: 3rem !important;
        padding: 2.4rem; 
        background-color: var(--bg-secondary); 
        border-radius: 1rem;
        max-width: 600px;
        overflow: hidden;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        width: 100%;
    }

    form label {
        text-transform: capitalize;
        color: var(--color-secondary);
        font-weight: 600;
        font-size: var(--text-base);
    }

    form input, form textarea {
        all: unset;
        box-sizing: border-box;
        background: var(--bg-primary);
        padding: 0.8rem;
        width: 100%;
        border-radius: 5px;
        color: var(--color-primary);
        font-size: var(--text-base);
        width: 100%;
    }

    form input::placeholder, form textarea::placeholder {
        color: var(--color-secondary);
        opacity: 0.7;
    }

    /* autocompletion input color */
    input:-webkit-autofill {
        -webkit-box-shadow: 0 0 0 1000px var(--bg-primary) inset !important;
    }

    textarea {
        height: 170px !important;
        resize: vertical;
    }

    *:focus {
        outline: solid 1px var(--color-tertiary) !important;
    }

    .name-container {
        display: flex;
        gap: 1.2rem;
        width: 100%;
    }

</style>