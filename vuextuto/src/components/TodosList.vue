<template>


<div>


<Todo v-for="(todo,index) in  todos " :key='index' :todo="todo"/>


</div>

</template>


<script>
import Todo from "./Todo"
import {mapState} from "vuex"

export default {
   components:{
       Todo,
   },
   computed:{
 /*      todos() {
           return this.$store.state.todos
       }
   }*/

   ...mapState({
       todos:"todos"
   })
   }

}

</script>


<style>

    
</style>
