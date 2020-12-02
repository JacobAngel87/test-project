<template>
    <div>
        <h1>{{message}}</h1>
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: [
        'message'
    ]
}
</script>

<style scoped>
h1 {
    background:darkslategray;
    color:white;
    text-align: center;
}
</style>