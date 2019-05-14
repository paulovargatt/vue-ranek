<template>
    <div id="app">
        <TheHeader/>
        <main id="main">
        <router-view/>
        </main>
        <TheFooter/>
    </div>
</template>

<script>
    import TheHeader from "@/components/TheHeader.vue"
    import TheFooter from "@/components/TheFooter.vue"

    export default {
        components: {
            TheHeader,
            TheFooter
        }
    }
</script>

<style>
ul{list-style: none}

    body{
        font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
        color: #345;
        background: url("./assets/pattern.svg") repeat top;
        padding: 0;
        margin: 0;
    }
    
    a{
        text-decoration: none;
        color: #345;
    }
    *{
        box-sizing: border-box;
    }

    img {
        max-width: 100%;
        display: block;
    }

    .btn{
        display: block;
        padding: 10px 30px;
        background: #87f;
        border-radius: 4px;
        color: #fff;
        text-align: center;
        font-size: 1rem;
        box-shadow: 0 4px 8px rgba(30,60,90,0.2);
        transition: all 0.3s;
        border: none;
        font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
        cursor: pointer;
    }
    .btn:hover{
        background: #65d;
        transform: scale(1.1);
    }

    #app{
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    main#main{
        flex: 1;
    }
</style>
