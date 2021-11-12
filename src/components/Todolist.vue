<template>
    <div class="Todolistcontain">
<h1 class="titleheading">Todo App</h1>
<todoInput :addtodo="addtodo"/>
<Todo  :todo="Todo" @deletetodo="deletetodo"/>

<div class="pendingTaskcontainer">
    <p>You have {{Todo.length}} Pending Task </p>

    <button class="cleartodoButton" @click="ClearTodoList">Clear All</button>
</div>


    </div>
</template>

<script>
import Todo from './Todo.vue'
import TodoInput from './TodoInput.vue'
 import { uuid } from 'vue-uuid';  
    export default {
  components: { TodoInput, Todo },
        name:"Todolist",
       
        data() {
            return {
                Todo:[
                    {
                    Task:"bye a new Gaming Laptop",
                    id:uuid.v1()

                    },
                    {
                    Task:"Complete a previous Task",
                    id:uuid.v1()

                    }
                    ],
                    NumberofPendingTodo:""
            }
        },
        methods: {
            addtodo(Tododata){
            this.Todo.push({Task:Tododata.Task , id:Tododata.id})
            } ,

            deletetodo(td){
         this.Todo = this.Todo.filter(todoli => todoli.id !==td.id)
            },

            ClearTodoList(){
               this.Todo = []
            }
        },
    }
</script>

<style scoped>

*{
padding: 0;
margin: 0;
box-sizing: border-box;
}

.Todolistcontain{
    max-width: 25.25rem;
    background-color: white;
    margin:0 auto;
    padding: 1rem;
}
.titleheading{
    font-weight: bold;

margin: 1rem 0;
}

.pendingTaskcontainer{
    display: flex;
    justify-content: space-between;
}

.cleartodoButton{
    padding: 0.3rem 0.5rem;
    font-size: 0.4;
    background-color: #8D4AE8;
    max-width: 5rem;
    border-radius: 0.2rem;
}

</style>