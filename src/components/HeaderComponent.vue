<script setup>



</script>

<template>

    <nav id="navbar">
        <div class="nav-content">
            <div class="logo">Vue JS Demo</div>
            <ul>
                <li><a href="#TI">Text Interpolation</a></li>
                <li><a href="#RHTML">Raw HTML</a></li>
                <li><a href="#AB">Attribute Binding</a></li>
                <li><a href="#JSE">JavaScript Expressions</a></li>
                <li><a href="#DC">Directivas</a></li>
                <li><a href="#CR">Conditional Rendering</a></li>
                <li><a href="#LR">List Rendering</a></li>
                <li><a href="#EH">Event Handling</a></li>
            </ul>
        </div>
    </nav>

</template>

<style scoped>
nav {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 18px 0;
    z-index: 1000;
    transition: background 0.3s ease, padding 0.3s ease, border-color 0.3s ease;
    background: rgba(3, 7, 18, 0.65);
    border-bottom: 1px solid transparent;
    backdrop-filter: blur(18px) saturate(180%);
    -webkit-backdrop-filter: blur(18px) saturate(180%);
}

nav.scrolled {
    background: rgba(2, 6, 23, 0.9);
    border-bottom-color: rgba(255, 255, 255, 0.08);
    padding: 12px 0;
}

.nav-content {
    width: min(95%, 90vw);
    margin: 0 auto;
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    gap: 32px;
}

.logo {
    font-weight: 600;
    font-size: 16px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--text-muted);
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 32px;
}

nav li a {
    color: var(--text-muted);
    text-decoration: none;
    font-size: 12px;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    transition: color 0.3s ease, opacity 0.3s ease;
}

nav li a:hover {
    color: #fff;
    opacity: 1;
}

</style>