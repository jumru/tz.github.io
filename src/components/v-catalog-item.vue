<template>
    <div class ="v-catalog-item">
        <img class="v-catalog-item__images" :src= "'/src/assets/images/'+ product_data.image" alt="img">
        <p class="v-catalog-item__name">{{product_data.name}}</p>
        <p class="v-catalog-item__price">Стоимость: {{product_data.price}}</p>
        <button class="v-catalog-item__add_to_cart_btn btn" @click="getMoney">Купить работу</button>    
    </div>
</template>

<script>
    export default{
        name: 'v-catalog-item',
        components:{},
        props: {
            product_data:{
                type: Object,
                default (){
                    return{}
                }
            }
        },
        data() {
            return{

            }
        },
        computed:{},
        methods:{
            getMoney(){
                alert('Перевод по номеру телефону на сумму: ' + this.product_data.price)
            }
        }
    }


</script>

<style lang="scss">
@import './src/assets/styles/variables.scss';
.v-catalog-item{
    min-width: 200px;
    margin-top: 10px;
    border-radius: 10px;
    transition: transform 500ms ease;
    flex-basis: 25%;
    background: white;
    box-shadow: 0 0 4px 0 #36363696;
    padding: $padding *2;
    margin-bottom: $margin*2;
    margin-left: $margin;
    &__images{
        width: 100px;
    }
} 
.v-catalog-item:hover{
    transform: scale(1.05) ;
}

.btn{
    background: #e3dc4b;
    color: rgb(7, 5, 5);
    border-radius: 10px;
    border: 1px solid #b99935;
    padding: 5px 10px;
    cursor: pointer;
    
}


</style>