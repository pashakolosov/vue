<template>
    <postform @create="createPost"/>
    <postlist :posts="posts" />
</template>

<script>
import Postform from './components/Postform.vue';
import Postlist from './components/Postlist.vue';

export default {
    components: {
        Postform, Postlist
    },
    data() {
        return {
            posts: [
                {id:1, title: 'aboout js', content: 'javascript is a very popular programming language'},
                {id:2, title: 'aboout js2', content: 'javascript is a very popular programming language2'},
                {id:3, title: 'aboout js3', content: 'javascript is a very popular programming language3'},
            ],
        }
    },
    methods: {
        createPost(post) {
            const obj = {
                title: post.title,
                content: post.content
            }
            
            if (obj.title && obj.content) this.posts.push(obj)
        },   
    }
}
</script>

<style>
body {
    background-image: url('../21-211580_stunning-white-polygon-wallpaper-images-for-free-download.png');
    background-size: cover;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: cursive;
}

.create__post {
    margin: 0 auto;
    padding: 15px;
    border: 1px solid black;
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.397);
    width: 70%;
}

input {
    padding: 10px;
    margin: 10px;
    border-radius: 5px;
    width: 100%;
}

input:focus {
    box-shadow: 1px 1px 20px rgba(0, 19, 128, 0.288);
}

button {
    align-self: flex-end;
    width: 200px;
    padding: 10px;
    margin: 10px;
    border-radius: 5px;
    color: teal;
    border: 2px solid teal;
    transition: box-shadow .5s;
}

button:hover {
    box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.158);
}

button:active {
    color: black;
    border: 2px solid black;
}

</style>