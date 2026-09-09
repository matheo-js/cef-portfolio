<script setup>
    import { ref } from 'vue'
    import { RouterLink } from 'vue-router'

    const sectionSelected = ref('presentation') 
</script>

<template>

    <header>
        <nav>
            <div class="center flex" style="padding: 1.5rem;">
                <h1> 
                    <RouterLink to="/" :class="{'active' : sectionSelected === 'presentation'}" @click="sectionSelected = 'presentation'">MT</RouterLink> 
                 </h1>
                
                <ul>
                    <li>
                        <a href="#presentation" :class="{'active' : sectionSelected === 'presentation'}" @click="sectionSelected = 'presentation'">Présentation</a>
                    </li>

                    <li>
                        <a href="#realisation" :class="{'active' : sectionSelected === 'realisation'}" @click="sectionSelected = 'realisation'">Réalisations</a>
                    </li>
                    
                    <li>
                        <a href="#contact" :class="{'active' : sectionSelected === 'contact'}" @click="sectionSelected = 'contact'">Contact</a>
                    </li>
                </ul>

            </div>
        </nav>
    </header>

</template>


<style scoped>

    nav {
        background-color: white;
        border-bottom: 1px solid var(--color-primary);
        box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
    }

    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
    }

    nav h1 {
        font-size: var(--text-lg);
        text-transform: uppercase;
        font-weight: bold;
        cursor: pointer;
    }

    nav h1 a {
        text-decoration: none !important;
        color: var(--color-primary);
    }

    nav ul {
        display: flex;
        gap: 1.3rem; 
        font-size: var(--text-base);
    }

    nav ul a {
        text-decoration: none;
        color: var(--color-secondary);
        font-weight: 300;
    }

    nav ul a:hover {
        opacity: 0.6;
    }

    .active {
        color: var(--color-primary);
        text-decoration: underline;
        text-underline-offset: 5px;
    }

    .active:hover {
        opacity: 1 !important;
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: space-between; 
    }

</style>