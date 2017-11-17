<template>
    <div id="app">
        <div class="transitionLine"></div>
        <router-view/>
    </div>
</template>
<script>
    export default {
        name: "app"
    };
</script>
<style lang="less" rel="stylesheet/less">
    @import "./assets/less/main";
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
        img {
            filter: sepia(120);
        }
        .transitionLine {
            width: 0;
            height: 2px;
            background-color: transparent;
        }
    }
</style>