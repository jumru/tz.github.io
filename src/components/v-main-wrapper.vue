<template>
    <div class ="v-main-wrapper">
    
        <v-catalog />  
        
    </div>
</template>

<script>
    import vCatalog from './v-catalog.vue'
    import vCart from './v-cart.vue'


    export default{
        name: 'v-main-wrapper',
        components:{
            vCatalog,
            vCart,
        },
        props: {},
        date() {
            return{
                title: 'Main wrapper'
            }
        },
        computed:{},
        methods:{},
        watch: {},
        mounted(){
            console.log('Hello Im alive')
        }
    }


</script>

<style> 
    .v-main-wrapper {
    max-width: 900px;
    border-radius: 10px;
    padding: 30px;
    background: linear-gradient(90deg, #00dec0ad 0%, #03c7ad60 100%);
    text-align: center;
    justify-content: center;
    align-items: center;
    place-items: center;
    color: #000000;
    margin: auto;
    }
</style>