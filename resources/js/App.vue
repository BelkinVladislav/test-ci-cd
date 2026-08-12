<script setup>
import { ref } from 'vue';

const clicks = ref(0);
</script>

<template>
    <main class="app-shell">
        <section class="card">
            <p class="eyebrow">Laravel + Vue</p>
            <h1>Проект готов к работе!</h1>
            <p class="description">
                Фронтенд работает на Vue 3, а сборка и горячее обновление — через Vite.
            </p>
            <button type="button" @click="clicks += 1">
                Нажато: {{ clicks }}
            </button>
        </section>
    </main>
</template>

<style scoped>
.app-shell { display: grid; min-height: 100vh; place-items: center; padding: 2rem; background: linear-gradient(135deg, #f8fafc, #e0e7ff); color: #0f172a; font-family: Inter, ui-sans-serif, system-ui, sans-serif; }
.card { max-width: 38rem; padding: 3rem; border-radius: 1.5rem; background: #fff; box-shadow: 0 20px 50px rgb(15 23 42 / 12%); }
.eyebrow { margin: 0 0 .75rem; color: #4f46e5; font-weight: 700; letter-spacing: .08em; text-transform: uppercase; }
h1 { margin: 0; font-size: clamp(2rem, 5vw, 3.5rem); line-height: 1.1; }
.description { margin: 1.25rem 0 2rem; color: #475569; font-size: 1.125rem; line-height: 1.6; }
button { cursor: pointer; border: 0; border-radius: .75rem; padding: .8rem 1.2rem; background: #4f46e5; color: #fff; font: inherit; font-weight: 700; }
button:hover { background: #4338ca; }
</style>
