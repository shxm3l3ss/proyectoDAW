<script setup>

import { ref } from 'vue';

let messageHTML = "<h2>v-html (Inyectar HTML al DOM)</h2><p>Este código es inyectado al DOM por medio de la directiva v-html</p>";

</script>

<template>

    <section class="section" id="RHTML">
        <div class="section-content">
            <div class="section-text">
                <h2>Raw HTML</h2>
                <p>Se refiere al código HTML mostrando o insertado directamente, 
                    sin aplicar estilos ni renderizarlo como elementos visuales. <br/>
                    <br/>
                    Para generar HTML real, es necesario usar la directiva v-html
                </p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content" v-html="messageHTML">
                    
                </div>
            </div>
        </div>
    </section>


</template>

<style scoped>
.section {
    padding: 140px 5vw;
    display: flex;
    justify-content: center;
    position: relative;
    z-index: 1;
}

.section::before {
    content: '';
    position: absolute;
    inset: 20px;
    background: rgba(255, 255, 255, 0.015);
    border-radius: 36px;
    z-index: -1;
}

.section-content {
    width: min(1200px, 90vw);
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 50px;
    align-items: center;
    background: rgba(2, 6, 23, 0.75);
    border-radius: 36px;
    border: 1px solid rgba(255, 255, 255, 0.08);
    padding: 60px;
    backdrop-filter: blur(20px);
}

.section-demo {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
}

.section-demo-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    width: 100%;
}

.section-demo-content input {
    width: 50%;
    height: 20px;
    padding-left: 5px;
    background-color: transparent;
    color: white;
    border-radius: 30px;
    border: 2px solid white;
}
.section-demo-content p{
    margin: 0;
}
.section h2 {
    color: white;
    margin: 0;
}

.section p {
    color: white;
}
</style>