<script setup>

import HeaderComponent from './components/HeaderComponent.vue';

import JSEComponent from './components/JSEComponent.vue';

import DirectivesComponent from './components/DirectivesComponent.vue';

import CRComponent from './components/CRComponent.vue';

import LRComponent from './components/LRComponent.vue';

import EHComponent from './components/EHComponent.vue';

import ABComponent from './components/ABComponent.vue';

import RawHTMLComponent from './components/RawHTMLComponent.vue';

import TIComponent from './components/TIComponent.vue';


</script>

<template>

  <HeaderComponent></HeaderComponent>

  <TIComponent></TIComponent>

  <RawHTMLComponent></RawHTMLComponent>

  <ABComponent></ABComponent>

  <JSEComponent></JSEComponent>

  <DirectivesComponent></DirectivesComponent>

  <CRComponent></CRComponent>

  <LRComponent></LRComponent>

  <EHComponent></EHComponent>

</template>

<style>

html{
  scroll-behavior: smooth;
}

:root {
    --bg-primary: #030712;
    --bg-secondary: #0b1121;
    --surface: rgba(255, 255, 255, 0.02);
    --surface-strong: rgba(255, 255, 255, 0.06);
    --accent: #8b5cf6;
    --accent-secondary: #0ea5e9;
    --text-primary: #f8fafc;
    --text-muted: rgba(248, 250, 252, 0.7);
    --border: rgba(255, 255, 255, 0.15);
    --shadow-soft: 0 30px 80px rgba(3, 7, 18, 0.6);
}

body {
    font-family: 'Inter', 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    color: var(--text-primary);
    line-height: 1.6;
    background: radial-gradient(circle at 10% 20%, #111733, transparent 45%),
                radial-gradient(circle at 80% 0%, #3b0764, transparent 35%),
                var(--bg-primary);
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
    margin: 0;
}

body::before,
body::after {
    content: '';
    position: fixed;
    width: 60vw;
    height: 60vw;
    background: radial-gradient(circle, rgba(139, 92, 246, 0.14), transparent 70%);
    filter: blur(40px);
    z-index: -2;
    pointer-events: none;
}

body::before {
    top: -20%;
    right: -10%;
}

body::after {
    bottom: -20%;
    left: -10%;
    background: radial-gradient(circle, rgba(14, 165, 233, 0.12), transparent 70%);
}

</style>