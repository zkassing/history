<template>
    <ul>
        <li v-if="items" v-for="item in items" :data-id="item.e_id">
            <h3>{{item.title}}</h3>
            <span>{{item.date}}</span>
        </li>
    </ul>
</template>

<script>
    export default{
        props:["items"]
    }
</script>

<style>
    
</style>
