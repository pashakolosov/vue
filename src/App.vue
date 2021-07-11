<template>
    <div>count of likes: {{ likes }}</div>
    <div>count of dislikes: {{ dislikes }}</div>
    <button @click="likes++">likes</button>
    <button @click="dislikes++">dislikes</button>
</template>

<script>
export default {
    data() {
        return {
            likes: 0,
            dislikes: 0
        }
    }
}
</script>

<style>

</style>