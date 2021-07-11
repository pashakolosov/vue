<template>
    <div v-for="elem in posts"  class="post">
        <div><strong>title: </strong> {{ elem.title }} </div>
        <div><strong>description</strong> {{ elem.content }} </div>
    </div>
</template>

<script>
    export default {
        props: {
            posts: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style   scoped>
    .post {
    background: rgba(255, 255, 255, 0.445);
    padding: 15px;
    margin: 10px auto;
    border: 2px solid teal;
    border-radius: 5px;
    width: 70%;
    }
</style>