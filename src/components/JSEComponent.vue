<script setup>

import { ref } from 'vue';

let message = ref("Hola a todos");

</script>

<template>

    <section class="section" id="JSE">
        <div class="section-content">
            <div class="section-text">
                <h2>JavaScript Expressions</h2>
                <p v-pre>En Vue.js, las JavaScript Expressions (JSE) permiten insertar fragmentos de código JavaScript
                    directamente en las plantillas para generar contenido dinámico.
                    Estas expresiones, envueltas en llaves dobles {{ }} , transforman o manipulan valores antes de
                    mostrarlos en la interfaz.
                    Por ejemplo, pueden realizar operaciones matemáticas, concatenar texto, aplicar condiciones simples
                    o acceder a propiedades de objetos del componente.</p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <input type="text" v-model="message">
                    <h2>Texto normal</h2>
                    <p>{{ message }}</p>
                    <h2>Texto al revés</h2>
                    <p>{{ message.split(' ').reverse().join(' ') }}</p>
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
    box-shadow: var(--shadow-soft);
    backdrop-filter: blur(20px);
}

.section-demo {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
}
.section-demo-content{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap:20px;
    width: 100%;
}

.section-demo-content input{
    width: 50%;
    height: 20px;
    padding-left: 5px;
    background-color: transparent;
    color: white;
    border-radius: 30px;
    border: 2px solid white;
}

.section h2 {
    color: white;
    margin: 0;
}

.section p {
    color: white;
}
</style>