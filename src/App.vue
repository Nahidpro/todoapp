<template>
<div class="container">


<todolist/>
</div>



</template>

<script>
import Todolist from './components/Todolist.vue'


export default {
  name: 'App',
  components: {
    Todolist
   
  }
}
</script>

<style scoped>

.container{
background: rgb(80,147,226);
background: linear-gradient(0deg, rgba(80,147,226,1) 0%, rgba(98,215,207,1) 100%, rgba(0,212,255,1) 100%); 
padding: 2rem;

}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;



}
</style>
