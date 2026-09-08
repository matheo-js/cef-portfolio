<script setup>

    const props = defineProps({
        project : {
            type : Object, 
            required : true 
        }
    })

    const emit = defineEmits(['close'])

</script>


<template>

    <div class="modale-content" @click.self="emit('close')">

        <div class="modal">

            <img :src="'./img/' + project.image" :alt="'image du projet' + project.title">

            <h3> {{ project.title }} </h3>
            <p> {{ project.description }} </p>

            <button @click="emit('close')">Fermer</button>

        </div>

    </div>

</template>

<style scoped>

    .modale-content {
        position: fixed;
        display: flex;
        align-items: center;
        justify-content: center;
        background: rgba(31, 31, 31, 0.433);
        width: 100vw;
        padding: 1.5rem;
        height: 100vh;
        overflow: hidden;
        top: 50%;
        left: 50%;
        backdrop-filter: blur(3px);
        transform: translate(-50%, -50%);
    }

    .modal {
        background: white;
        width: 590px;
        max-width: 100%;
        overflow: hidden;
        border-radius: 10px;
        padding: 2rem;
    }

    .modal img {
        width: 100%;
        height: 200px;        
        object-fit: cover;
        border-radius: 10px;   
    }

    .modal h3 {
        margin-top: 1rem; 
        font-size: var(--text-lg);
        color: var(--color-primary);
        text-transform: uppercase;
        font-weight: bold;
        text-wrap: balance;
    }

    .modal p {
        margin-top: 0.2rem; 
        font-size: var(--text-base);
        color: var(--color-secondary);
    }    

</style>