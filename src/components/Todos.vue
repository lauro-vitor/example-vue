<template>
    <div>
        <form v-on:submit.prevent="addNewTodo">
            <label for="new-todo">Tarefa:</label>
            <input 
                id="newTodo" 
                placeholder="Ex: alimentar o Gato"
                v-model="newTodoText">
            <button type="submit">Adicionar</button>
        </form>
        <ul>
            <li 
                v-for="(todo, index) in todos" 
                v-bind:key="todo.id"
                v-bind:title="todo.title">
               {{todo.id}} = {{todo.title}}
               <button v-on:click="removeTodo(index)">Apagar todo</button>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    data: () =>({
        newTodoText: '',
        todos:[
            {
                id: 1,
                title: 'Lavar os pratos'
            },
            {
                id: 2,
                title: 'Tirar o Lixo!'
            },
            {
                id: 3,
                title: 'Cortar grama!'
            }
        ],
        nextTodoId: 4,
    }),

    methods:{
        addNewTodo: function () {
            this.todos.push({
                id: this.nextTodoId ++,
                title: this.newTodoText,
            });
            this.newTodoText =  '';
        },
        removeTodo: function(index) {
            this.todos.splice(index,1);
        }
    }
}
</script>
<style scoped>

</style>