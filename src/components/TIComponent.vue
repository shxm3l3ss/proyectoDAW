<script setup>

import { ref } from 'vue';

let inputValue = ref("");

</script>

<template>

    <section class="section" id="TI">
        <div class="section-content">
            <div class="section-text">
                <h2>Text Interpolation</h2>
                <p v-pre>Es la forma más básica de enlace de datos en la cual se usa la sintaxis “Mustache” o llaves dobles {{ }}.  
                    Estas llaves dobles se usan básicamente para reemplazar automáticamente las expresiones con sus valores correspondientes. 
                </p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <h2>Escribe un mensaje:</h2>
                <input type="text" v-model="inputValue" maxlength="60">
                <h2>Resultado</h2>
                <p>{{ inputValue }}</p>
                <p>Cantidad Caracteres: {{ inputValue.length }}</p>
                <h2>Texto Mayúscula</h2>
                <p>{{ inputValue.toUpperCase() }}</p>
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

.section-demo input {
    width: 50%;
    height: 20px;
    padding-left: 10px;
    padding-right: 10px;
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
    margin: 0;
}
</style>