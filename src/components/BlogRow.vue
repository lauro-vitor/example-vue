<template>
    <div id="globalContent">
        <div id="content">
            <slot ></slot>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style  scoped>
    div#globalContent{
        border:1px solid green;
    }
    div#content {
        margin: 10px;
        padding:10px;
        border: 1px solid red;
    }
</style>