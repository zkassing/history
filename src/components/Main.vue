<template>
    <div>
        <List :items="items"></List>
    </div>
</template>

<script>
    import List from "./List.vue"
    export default {
        data () {
            return {
                items:[]
            }
        },
        components:{
            List
        },
        created(){
            this.$http.jsonp("http://v.juhe.cn/todayOnhistory/queryEvent.php?key=7916c7a8e8e94ef7576ff1117dbc436d&dtype=jsonp&date=1/1").then(response=>{
                this.items = response.body.result
            })
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
