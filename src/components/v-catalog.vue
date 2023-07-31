<template>
    <div class ="v-catalog">
        <h1>Каталог</h1> 
        <div class="v-catalog__list">
        <v-catalog-item 
        v-for="product in products"
        :key="product.article"
        :product_data="product"
        />
        </div>
    </div>
</template>

<script>
    import vCatalogItem from './v-catalog-item.vue';

    export default{
        name: 'v-catalog',
        components:{
            vCatalogItem
        },
        props: {},
        data() {
            return{
                products: 
            [
                {
                image: "1.jpg",
                name: "Задание 1",
                price: 100,
                article: "T1",
                available: true,
                },
                {
                image: "2.jpg",
                name: "Задание 2",
                price: 200,
                article: "T2",
                available: true,

                },
                {
                image: "3.jpg",
                name: "Задание 3",
                price: 300,
                article: "T3",
                available: false,
                },
                {
                image: "4.jpg",
                name: "Задание 4",
                price: 400,
                article: "T4",
                available: true,

                },
                {
                image: "5.jpg",
                name: "Задание 5",
                price: 500,
                article: "T5",
                available: false,

                },
                {
                image: "6.jpg",
                name: "Задание 6",
                price: 600,
                article: "T6",
                available: true,

                }
            ]
            }
        },
        computed:{},
        methods:{},
        
    }


</script>

<style lang="scss"> 
@import './src/assets/styles/variables.scss';
    .v-catalog{
        &__list{
            display: flex;
            flex-wrap:wrap; 
            justify-content: space-between;
            align-items: center;
            
            
           
        }
    }
</style>