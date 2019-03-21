<template>
  <div id="app">
   <!-- <car brand="Fiat" model="Uno" />
   <car brand="Opel">
     <p style="color:green">Kadet</p>
   </car> -->
   <base-layout>
      <template slot="header">
        <h1>This is header</h1>

       </template>

       <!-- <TodoList :todos="todos"/> -->

       <TodoList :todos="todos">

         <div slot-scope="todoScope">
           <!-- pristupamo informacijama iz child komponente -->
           <h3>{{todoScope.todo.text}}</h3>
          <h4> {{todoScope.todo.isCompleted ? "bravo" : "neee"}}</h4>
         </div>

       </TodoList>
    

     
        <template slot="footer">
        <h1>This is footer</h1>

        </template>
    </base-layout>

  </div>
</template>

<script>
import Car from './components/Car.vue'
import BaseLayout from './components/BaseLayout'
import TodoList from './components/TodoList.vue'
export default {
  name: 'app',
  components: {
    Car,
    BaseLayout,
    TodoList
  },
  data(){
    return {
      todos:[
        {id:1, text:"todo1",isCompleted:false},
        {id:2, text:"todo2",isCompleted:false},
        {id:3, text:"todo3",isCompleted:true},
        
        
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
