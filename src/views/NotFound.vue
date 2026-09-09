<template>
    <div class="center not-found">
        <p class="job-title">404</p>
        <h1>Page non trouvée</h1>
        <p>La page que vous recherchez n'existe pas.</p>
        <router-link to="/">Retour à l'accueil</router-link>
    </div>
</template>


<style scoped>
    .not-found {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 3rem 1.5rem;
    }

    .not-found .job-title {
        font-size: var(--text-base);
        color: #28A471; 
        margin-top: 0;
        margin-bottom: 0.5rem;
        text-transform: uppercase;
        font-weight: bold;
    }

    .not-found h1 {
        font-size: var(--text-xxl);
        color: var(--color-primary);
        text-transform: uppercase;
        font-weight: bold;
        text-wrap: balance;
    }

    .not-found p {
        color: var(--color-secondary);
        font-size: var(--text-base);
        line-height: 1.5;
        margin-top: 1rem;
        text-wrap: balance;
    }
</style>