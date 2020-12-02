<template>
    <div>
        <Tasklist v-for="task in task" v-bind:aTask= "task" v-bind:key= "task.id"></Tasklist>
    </div>
</template>
<script>
import Tasklist from './Tasklist.vue'
export default {
    name: "Task",
    props:['task'],
    components: {
        Tasklist
    }    
}
</script>
<style scoped>

</style>