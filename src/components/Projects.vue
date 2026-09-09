<script setup>
    import {ref} from "vue"

    import {projects} from "@/data/projects.js"

    import Card from "@/components/Card.vue"
    import Modale from "@/components/Modale.vue"

    const selectedProject = ref(null)
    const openModale = ref(false)

    const openModal = (project) => {
        selectedProject.value = project
        openModale.value = true
    }

    const closeModal = () => {
        selectedProject.value = null
        openModale.value = false
    }

</script>

<template>


    <section id="realisation"  style="background-color: white;">

        <div class="center projet-container">
            <p class="job-title">02 — mes réalisations</p>
            <h2>Voici quelques-uns de mes projets</h2>
            <p>Mes réalisations touchent principalement au développement web, avec des projets personnels et des projets réalisés dans le cadre de ma formation.</p>

            <div class="card-content">
                <Card v-for="p in projects" :key="p" :project="p" @click="openModal(p)" />
            </div> 

            <Modale v-if="openModale" :project="selectedProject" @close="closeModal" />
        </div>

    </section>

</template>



<style scoped>

    .projet-container  {
        padding: 3rem 1.5rem;
    }

    .projet-container h2 {
        font-size: var(--text-xl);
        color: var(--color-primary);
        text-transform: uppercase;
        font-weight: bold;
        text-wrap: balance;
    }

    .projet-container p {
        color: var(--color-secondary);
        font-size: var(--text-base);
        line-height: 1.5;
        margin-top: 1rem;
        text-wrap: balance;
    }
    
    .card-content {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1.5rem; 
        margin-top: 3rem !important; 
    }

    /* responsive */
    @media screen and (max-width: 900px) 
    {
        .card-content {
            grid-template-columns: repeat(2, 1fr); 
        }
    }

    @media screen and (max-width: 650px) 
    {
        .card-content {
            grid-template-columns: repeat(1, 1fr);
        }
    }
</style>