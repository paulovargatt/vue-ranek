<template>
    <section class="produtos-container">
        <div v-for="prod in produtos" :key="prod.id">
            <img v-if="prod.fotos" :src="prod.fotos[0].src" alt="">
            <h2 class="preco">{{prod.preco}}</h2>
            <h2 class="titulo">{{prod.nome}}</h2>
            <p>{{prod.descricao}}</p>
        </div>
    </section>
</template>

<script>

    export default {
        data(){
            return {
                produtos: null
            }
        },
        methods: {
            getProducts() {
                fetch("http://localhost:8080/api//produtos/ranek.json").then(response => response.json()).then((res) => {
                    this.produtos = res.produto
                   // console.log(this.produtos)
                })
            }
        },
        created() {
            this.getProducts();
        }
    }
</script>

<style scoped>

</style>
