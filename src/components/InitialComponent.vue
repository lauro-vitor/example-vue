<template>
    <div>
        <p>Recebendo uma props</p>
        <h2>{{title}}</h2>
        <p>{{post}}</p>
    </div>
</template>
<script>
export default {
    data: () => ({
    }),
    props:{
        title:{
            type:String,
            required: true
        },
        post: {
            type: String,
            required: true
        }
    }
}
</script>
<style scoped>

</style>