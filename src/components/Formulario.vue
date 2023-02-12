<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>


<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp"
                    type="text" placeholder="Enter the task description" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Send</button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-control">
                    <option value="todas">All Tasks</option>
                    <option value="pendentes">Pending Tasks</option>
                    <option value="finalizadas">Finished Tasks</option>
                </select>
            </div>
        </div>
    </form>
</template>