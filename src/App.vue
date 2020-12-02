<template>
  <div id="app">
    <Header message="Hello?"></Header>
    <Task v-bind:task=tasks></Task>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Task from './components/Task.vue'
import axios from 'axios';

export default {
  name: "App",
  components: {
    Header,
    Task
  },
  data() {
    return {
      tasks: [
        {id:0, title:"Learn HTML", completed: true},
        {id:1, title:"Learn JavaScript", completed: false},
        {id:2, title:"Learn JS Framework Vue", completed: false}
      ]
    }
  },
  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/todos')
    .then((response)=>{
      this.tasks = response.data;
    })
  }
};
</script>
<style>
* {
  margin: 0px;
  padding: 0px;
}
</style>