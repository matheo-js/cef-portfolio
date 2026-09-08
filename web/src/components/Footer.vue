<template>

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