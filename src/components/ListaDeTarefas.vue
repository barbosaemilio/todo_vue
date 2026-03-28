<script setup>
const props = defineProps(['tarefas'])
</script>
<template>
  <ul class="list-group mt-4">
    <li class="list-group-item" v-for="tarefa in props.tarefas">
      <input @change="evento => tarefa.finalizada = evento.target.checked" :checked="tarefa.finalizada"
        :id="tarefa.titulo" type="checkbox">
      <label :class="{ done: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">
        {{ tarefa.titulo }}
      </label>
    </li>
  </ul>
</template>


<style scoped>
.list-group-item {
  background-color: #fff;
  border: 1px solid #eee;
  margin-bottom: 8px;
  border-radius: 6px !important;
  display: flex;
  align-items: center;
  transition: transform 0.2s ease;
}

.list-group-item:hover {
  background-color: #fafafa;
}

input[type="checkbox"] {
  accent-color: #000;
  /* Checkbox fica preto ao marcar */
  width: 18px;
  height: 18px;
  cursor: pointer;
}

label {
  cursor: pointer;
  color: #333;
  font-weight: 500;
}

.done {
  text-decoration: line-through;
  color: #999;
  /* Cinza para tarefas finalizadas */
  font-style: italic;
}
</style>