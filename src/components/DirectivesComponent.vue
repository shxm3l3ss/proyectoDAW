<script setup>

import { ref } from 'vue';

let radioValue = ref(true);

let movies = ["Batman","Escuadron Suicida", "Avengers"];

</script>

<template>

    <section class="section" id="DC">
        <div class="section-content">
            <div class="section-text">
                <h2>Directivas</h2>
                <p v-pre>Las directivas son un elemento clave del enfoque declarativo de Vue.js.  Se definen como atributos especiales del DOM que empiezan con el prefijo “v-“ y 
                    sirven para enlazar la estructura visual con la lógica reactiva del componente. Cada directiva tiene un propósito único y actúa como un puente entre los datos 
                    y el comportamiento del elemento HTML donde se aplica.</p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <h2>v-if</h2>
                    <input type="checkbox" v-model="radioValue">
                    <p v-if="radioValue">Sorpresa</p>
                    <h2>v-for</h2>
                    <div class="section-demo-content-for">
                        <p v-for="movie in movies">{{ movie }}</p>
                    </div>
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
.section-demo-content-for{
    display: flex;
    flex-direction: column;
    align-items: center;
}

.section-demo-content-for p{
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