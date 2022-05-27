<template>
    <div>
        <Post />
    </div> 
</template>

<script>
import Post from "../components/Post.vue"
export default {
    name: "PostList",

    components: {
        Post,
    },
    data() {
        return {
            posts :[],
        }
    },
    methods : {
        getPosts(){
            axios.get("http://127.0.0.1:8001/api/posts")
        }
    }

}
</script>

<style lang=scss scoped>

</style>