<template>
    <div class="inputgroup">
<input type="text" name="" id="" placeholder="Add Your new todo" v-model="tododata.Task">
<button @click="addtodo(tododata)">+</button>

    </div>
</template>

<script>
 import { uuid } from 'vue-uuid';  
    export default {
        name:'TodoInput',
        props:{
            addtodo:Function,
        },
        data() {
            return {
                tododata:{
                    Task:'',
                    id:uuid.v1()
                }
            }
        },
    }
</script>

<style  scoped>
.inputgroup{
   width: 100%;
   display: flex;
   box-sizing: border-box;
}

input, button{
    padding:0.1rem ;
    border-radius: 0.2rem;
    margin: 0.2rem;
}
input{
    flex: 7;
    padding-left: 2%;

}
button{
    flex: 0.5;
    background-color: #8D4AE8;
    color: white;
    font-size: 20px;
    font-weight: bold;
}



</style>