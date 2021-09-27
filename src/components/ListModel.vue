<template>    
    <li v-bind:value="index+1">{{item}}</li>
</template>

<script>
export default {
    name:'ListModel',
    props:['item','index']
}
</script>