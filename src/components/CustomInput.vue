<template>
    <input
        type="text"
        v-bind:value="value"
        v-on:input="$emit('input', $event.target.value)"
        v-bind:placeholder="placeHolder"
    />
</template>
<script>
export default {
    props:{
        value:String,
        placeHolder: String,
    }
}
</script>
<style scoped>
    input{
        margin: 10px;
        width: 80%;
    }
</style>