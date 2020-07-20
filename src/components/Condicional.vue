<!-- exemplos de renderização condicional-->
<template>
    <div id="main">
        <h1 v-if="awaesome">Vue é incrível!</h1>
        <p v-else>Oh não</p>
        <div v-if="type === 'A' || type === 'a'">
            A
        </div>
        <div v-else-if="type === 'B' || type === 'b'">
            B
        </div>
        <div v-else-if=" type === 'C' || type === 'c'">
            C
        </div>
        <div v-else>
            Não é A, B ou C
        </div>
    </div>  
</template>
<script>
export default {
    data: function() {
        return{
            awaesome: true,
            type:'a'
        }
    }
}
</script>
<style scoped>

</style>