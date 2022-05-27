<template>
    <div class="w-50 m-5 card-body text-center">
        <h3>{{ post.username}}</h3>
        <img :src= 'post.cover_url' :alt="post.username">
        <p class="p-2 text-center">{{post.description}} </p>
    </div>
</template>
<script>

export default {
    name: "Post",
        
    components: {},
    props: ["post"]
}
</script>

<style lang=scss scoped>

</style>