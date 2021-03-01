<template>
    <div>
        <span :class="{completed :todo.completed}" @click="toggleTodoStatus(todo)">{{todo.title}}</span>
    <button @click="deleteTodo(todo)">Delete</button>
    </div>
</template>


<script>

import {mapActions} from "vuex"
export default {
    name:"Todo",
    props:["todo"],

    methods:{

       ...mapActions({
           deleteTodo:"deleteTodo",
           toggleTodoStatus:"toggleTodoStatus"
       })

   /*     deleteTodo(){
            this.$store.dispatch("deleteTodo", this.todo)

        },
        toggleTodoStatus(){
            this.$store.dispatch('toggleTodoStatus', this.todo)
        }*/
    }


   

}
</script>


<style scoped>
.completed{
 text-decoration:line-through
}

</style>