<template>
    <div  class="todo todocontainer" v-for="td in todo" :key="td.id">
      <p >{{td.Task}} </p>
    
      <button @click="$emit('deletetodo', td)" > <fa icon="trash"/></button> 
     
 
    </div>
</template>

<script>
 
    export default {
        name:"Todo",
        props:{
            todo:Object
        },
        emits:['deletetodo'],
        data() {
            return {
              
            }
        },
        methods: {
            
        },
        
    }
</script>

<style scoped>
    .todocontainer{
        display: flex;
        justify-content: space-between;
    }
   .todo{
       background-color: #F2F2F2;
       padding-left: 0.5rem;
      font-size: 14px;
       margin:0.5rem 0;
   }
   p{
       flex: 7;
   }

   button{
       border-radius: 0.1rem;
       flex: 0.5;
       background-color: #E84D39;
   }



  
</style>