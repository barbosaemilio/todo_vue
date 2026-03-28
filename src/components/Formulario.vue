<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>
<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required type="text"
                    placeholder="Digite aqui sua tarefa" class="form-control">
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-control">
                    <option value="todas">Todas tarefas</option>
                    <option value="pendentes">Tarefas pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>

<style scoped>
form {
    background-color: #fff;
    padding: 25px;
    border-radius: 8px;
    border: 1px solid #e0e0e0;
}

.form-control {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 10px;
}

.form-control:focus {
    border-color: #000;
    box-shadow: 0 0 0 0.2rem rgba(0, 0, 0, 0.05);
}

.btn-primary {
    background-color: #000;
    border: none;
    color: #fff;
    font-weight: bold;
    transition: background-color 0.3s ease;
}

.btn-primary:hover {
    background-color: #333;
}

select.form-control {
    cursor: pointer;
    background-color: #f9f9f9;
}
</style>