<script setup>
const props = defineProps(['tarefasPendentes']);
</script>

<template>
    <header class="p-5 mb-4 mt-4 bg-light rounded-3">
        <h1>Minhas Tarefas</h1>
        <p>
            Você possui {{ tarefasPendentes }} tarefas pendentes
        </p>
    </header>
</template>

<style scoped>
header {
    background-color: #333 !important;
    /* Fundo preto */
    color: #fff;
    /* Texto branco */
    padding: 40px;
    border-radius: 8px;
    text-align: center;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h1 {
    font-weight: 700;
    letter-spacing: -1px;
    margin-bottom: 10px;
}

p {
    color: #ccc;
    /* Cinza claro para o subtítulo */
    margin: 0;
    font-size: 1.1em;
}
</style>