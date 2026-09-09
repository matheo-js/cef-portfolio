<script setup>
    import {projects} from "@/data/projects.js"
</script>

<template>

    <section id="presentation" class="center">
        <div class="presentation-container">

            <div class="presentation-text">
 
                <p class="job-title">01 — Présentation</p>

                <h2>Mon parcours & ma vision du web</h2> 

                <p>
                   Je m'appelle Mathéo, j'ai 18 ans et je suis étudiant en informatique, passionné par le développement web. Actuellement en deuxième année de formation (cursus Bac+2) de développeur web, je suis en pleine période d'apprentissage des technos front-end et back-end.
                </p>

            </div>

            <div class="image-container" :data-count-project="projects.length"></div>

        </div>
    </section>

</template>



<style scoped>

    .presentation-container {
        padding: 3rem 1.5rem;
    }

   .presentation-container h2 {
        color: var(--color-primary);
        font-size: var(--text-xxl);
        text-transform: uppercase;
        font-weight: 800;
        text-wrap: balance;
    }

    .presentation-container p {
        color: var(--color-secondary);
        font-size: var(--text-base);
        line-height: 1.5;
        margin-top: 1rem;
    }

    .presentation-container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 2em;
    }
 
    .presentation-container button {
        width: fit-content;
    }

    .image-container {
        position: relative;
        height: 260px;
        aspect-ratio: 1/1;
        background-image:
            url("/public/img/photo.png"), 
            linear-gradient(to right, var(--color-tertiary), var(--color-tertiary)); 
        border-radius: 50%;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

    .image-container::before {
        content: '';
        position: absolute;
        aspect-ratio: 1/1;

        top: -10px;
        left: -10px;
        right: -10px;
        bottom: -10px;

        border-radius: 50%;
        border: 1px solid black; 
        z-index: -1;
    }

    .image-container::after {
        content: attr(data-count-project);
        display: flex;
        overflow: hidden;
        align-items: center;
        justify-content: center;
        color: white;
        font-weight: bolder;
        position: absolute;
        aspect-ratio: 1/1;
        height: 50px;
        top: 0px;
        right: 0px;
        font-size: var(--text-base);  
        border-radius: 50%;
        box-shadow: 5px 4px 0 black;
        background: var(--color-quaternary);
    } 

    @media screen and (max-width: 900px) 
    {
        .presentation-container {
            flex-direction: column-reverse; 
        }
    }

</style>