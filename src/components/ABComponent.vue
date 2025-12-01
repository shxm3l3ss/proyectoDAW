<script setup>

import { ref } from 'vue';

let vbind = ref("red");

</script>

<template>

    <section class="section" id="AB">
        <div class="section-content">
            <div class="section-text">
                <h2>Attribute Binding</h2>
                <p>Hace referencia a la manera en que podemos mantener sincronizado el valor de dos variables, 
                    permitiéndonos conectar los datos de JavaScript con HTML. Esto permite que valores como id, src, href, class o 
                    style cambien automáticamente según el estado de sus datos. Cabe mencionar que existen dos tipos de binding:
                </p>
                <ul>
                    <li>Unidireccional: Directiva v-bind.</li>
                    <li>Bidireccional: Elementos de formulario y la directiva v-model.</li>
                </ul>

            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <h2>v-bind (Unidireccional)</h2>
                    <p :class="vbind">Color Texto: {{ vbind }}</p>
                    <h2>v-model (Bidireccional)</h2>
                    <p>Escribe "blue" o "red" segun el color que quieras en el texto</p>
                    <input type="text" v-model="vbind">
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
.red{
    color: red;
}
.blue{
    color: blue;
}
</style>