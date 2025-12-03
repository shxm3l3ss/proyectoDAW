<script setup>

import { ref } from 'vue';

let contador = ref(0);

</script>

<template>

    <section class="section" id="EH">
        <div class="section-content">
            <div class="section-text">
                <h2>Event Handling</h2>
                <p>El Event Handling en Vue.js permite capturar y responder a las acciones del usuario mediante la directiva v-on, 
                    la cual escucha eventos del DOM como click, input, submit, entre otros. Esta directiva conecta los eventos con 
                    métodos definidos en el componente, logrando que la interfaz reaccione de forma automática cuando el usuario interactúa.</p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <h2>v-on (Incrementar y Disminuir el contador)</h2>
                    <div class="section-demo-button-container">
                        <button @click="contador++">Incrementar</button>
                        <button @click="contador--">Disminuir</button>
                        <button v-show="false" v-on:click="contador++">v-on</button> <!--Directiva v-on completa-->
                    </div>
                    <p>Contador: {{ contador }}</p>
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
.section-demo-button-container{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 20px;
    width: 100%;
}

.section-demo-content p{
    margin: 0;
}
.section-demo-content button{
    border: 2px solid white;
    background-color: transparent;
    border-radius: 30px;
    color: white;
    width: 100px;
    height: 30px;
    transition-duration: 500ms;
}

.section-demo-content button:hover{
    border: 2px solid black;
    background-color: white;
    color: black;
    transition-duration: 500ms;
}

.section h2 {
    color: white;
    margin: 0;
}

.section p {
    color: white;
}
</style>