<template>
    <div class="container d-flex flex-column align-items-center">
        <Post v-for=" (post, index) in posts" :key= 'index' :post="post" />
        
    </div> 
</template>

<script>
import Post from "./Post.vue"
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
            axios.get("http://127.0.0.1:8000/api/posts/")
                .then((result)=>{
                    console.log(result.data.results.data);
                    this.posts = result.data.results.data;
                })
            .catch( (error) => {
                    console.warn(error);
                });
            
        }
    },
    created(){
        this.getPosts();
    }

}
</script>

<style lang=scss scoped>

</style>