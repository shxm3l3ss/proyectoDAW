<script setup>

import { ref } from 'vue';

let movies = ref([]);

let inputValue = ref("");

let showWarning = ref(false);

function addMovie(){
    if(movies.value.length <= 5){
        movies.value.push(inputValue.value);
        inputValue.value = "";
        showWarning.value = false;
    }else{
        showWarning.value = true;
    }
}

</script>

<template>

    <section class="section" id="LR">
        <div class="section-content">
            <div class="section-text">
                <h2>List Rendering</h2>
                <p>El List Rendering en Vue.js permite generar elementos de manera dinámica a partir de arreglos u objetos mediante la directiva v-for. 
                    Esta directiva crea una repetición de un bloque de plantilla por cada elemento presente en una lista, lo que facilita mostrar colecciones 
                    de datos sin tener que escribir cada elemento manualmente.</p>
            </div>
            <div class="section-demo">
                <h2>Demo</h2>
                <div class="section-demo-content">
                    <h2>v-for (Agrega peliculas a la lista)</h2>
                    <input type="text" v-model="inputValue" @keydown.enter="addMovie">
                    <div class="movie-list">
                        <p class="movie-list-item" v-for="movie in movies">{{ movie }}</p>
                    </div>
                    <p v-show="showWarning">Numero máximo de peliculas alcanzado</p>
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
    text-align: center;
}
</style>