<script setup>
    import { ref } from 'vue'
    import { RouterView } from 'vue-router' 

    const sectionSelected = ref('presentation') 
</script>

<template>
    <header>
        <nav>
            <div class="center flex" style="padding: 1.5rem;">
                <h1>MT</h1>
                
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
    
    <main>
        <RouterView />
    </main>

    <footer style="background: white;">
        
        <div class="center" style="padding: 1.5rem;">

            <div class="content-footer-item">

                <a href="https://github.com/matheo-js" target="_blank">
                    <i class="fa-brands fa-github"></i>
                </a>
                
                <a href="https://www.linkedin.com/in/matheo-th-aa656b400 " target="_blank">
                    <i class="fa-brands fa-square-linkedin"></i> 
                </a>

                <a href="mailto:matheo.js22@gmail.com">
                    <i class="fa-solid fa-envelope"></i>
                </a>

            </div>

            <small>© {{ new Date().getFullYear() }}. Tous droits réservés.</small>

        </div>        
    </footer>
</template>

<style scoped>

    nav {
        background-color: white;
        border-bottom: 1px solid var(--color-secondary); 
    }

    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
    }

    main {
        padding-top: 100px;
    }

    nav h1 {
        font-size: var(--text-lg);
        color: var(--color-primary);
        text-transform: uppercase;
        font-weight: bold;
        cursor: pointer;
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

    .active {
        color: var(--color-primary);
        text-decoration: underline;
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: space-between; 
    }

    footer {
        display: flex;
        flex-direction: column; 
        justify-content: center;
        align-items: center; 
    }
    
    footer small {
        font-size: var(--text-sm);    
        font-weight: 300;
        color: var(--color-secondary);
    }

    .content-footer-item {
        display: flex;
        gap: 1rem; 
        margin: auto;
        align-items: center;
        justify-content: space-between;
        width: fit-content;
    }

    .content-footer-item a {
        text-decoration: none;
        color: var(--color-secondary);   
        font-size: var(--text-xl);     
    }

    .content-footer-item a:hover {
        color: #28A471;
    }

</style>