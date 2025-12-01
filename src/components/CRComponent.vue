<script setup>

import { ref } from 'vue';

let showText1 = ref(false);

let showText2 = ref(false);

let inputValue = ref("");

function checkInputValue() {
    if (inputValue.value == "Vue JS") {
        showText1.value = ref(true);
    } else {
        showText1.value = (false);
    }
}


</script>

<template>

    <section class="section" id="CR">
        <div class="section-content">
            <div class="section-text">
                <h2>Conditional Rendering</h2>
                <p>El renderizado condicional en Vue.js permite mostrar o ocultar elementos de la interfaz según el
                    estado de los datos del componente.
                    Este concepto es clave para crear interfaces dinámicas donde la visibilidad de ciertos elementos
                    cambia con las acciones del usuario,
                    las validaciones o la lógica interna de la app.</p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <h2>v-if (Escribe Vue JS)</h2>
                    <input type="text" v-model="inputValue" @keyup="checkInputValue()">
                    <p v-if="showText1">v-if vuelve a renderizar el elemento</p>
                    <h2>v-show</h2>
                    <button @click="showText2 = !showText2">Haz Click</button>
                    <p v-if="showText2">v-show cambiar la propiedad display a none</p>
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