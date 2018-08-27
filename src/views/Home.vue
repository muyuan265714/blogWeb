<template>
    <div id="home">
    </div>
</template>

<script>
    export default {
        data(){
            return{
                activeIndex2: '1'
            }
        },
        methods:{
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }
</script>

<style lang="less">
    #home{
        height: 100%;
    }
</style>
