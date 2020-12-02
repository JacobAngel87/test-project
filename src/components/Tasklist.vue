<template>
    <div class="toolItem">
        <div v-bind:class="{isCompleted:aTask.completed}">{{aTask.title}}</div>
    </div>
</template>
<script>
export default {
    name: "Tasklist",
    props: [
        'aTask'
    ]    
}
</script>
<style scoped>
    .toolItem {
        background: #f4f4f4;
        padding:10px;
        border-bottom: 3px #cccc dotted
    }
    .isCompleted {
        text-decoration: line-through;
    }
</style>