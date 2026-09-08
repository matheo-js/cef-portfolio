<script setup>

    const props = defineProps({
        project : {type : Object, required : true}
    })

</script>

<template>

    <div class="card">
        <img :src="'./img/' + props.project.image" :alt="'image ' + props.project.title">
        <h3> {{ props.project.title }} </h3>
    </div>

</template>


<style scoped>

    .card {
        display: block;
        padding: 1.3rem;
        cursor: pointer;
        background: #E9F1FF;
        overflow: hidden;
        border-radius: 15px; 
    }

    .card:hover {
        opacity: 0.8;        
    }

    .card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
        border-radius: 5px;
        transition: all 0.3s ease;
    }

    .card h3 {
        margin-top: 1rem; 
        font-size: var(--text-base);
        /* font-weight: bold; */
        color: var(--color-primary);
        text-transform: uppercase;

        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }

    .card p {
        margin-top: 0.2rem; 
        font-size: var(--text-base);
        color: var(--color-secondary);
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }

</style>

