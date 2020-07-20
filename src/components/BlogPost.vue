<template>
    <div>
        <h2>{{title}}</h2>
        <p>{{post}}</p>
        
    </div>
</template>
<script>
export default {
    props:{
        title:String,
        post:String,
    }
}
</script>
<style scoped>

</style>