<template>
  <div class="container">
    <section class="title">
        <p>OUR PRODUCTS</p>
        <h1>All our delectable pastries are baked fresh in our kitchen every morning, and are made with all natural, all organic ingredients</h1>
        <button class="purpleBtn">Start shopping</button>
    </section>
    <section class="products">
        <div class="myProducts">
            <ourProducts
            v-for="(item, index) in items" :key="index"
            :item="item.pic"
            :itemName="item.name"
            :itemType="item.type"
            :itemPrice="item.price"
            :itemWeightPrice="item.weightPrice"
            />
        </div>
    </section>
  </div>
  
</template>

<script>
import ourProducts from "./ourProducts.vue";
export default {
    name: "OurProductsMain",
    components: {ourProducts,},
    data: function(){
        return{
            items: [
                {
                    pic:"choco-chip-cookies-400x510.jpg",
                    name:"Choco Chip Cookies",
                    type:"Cookies, Pastries",
                    price:"19.00",
                    weightPrice:"39.00"
                },
                 {
                    pic:"strawberry-jam-cookies-400x510.jpg",
                    name:"Strawberry Jam Cookies",
                    type:"Cookies, Pastries",
                    price:"24.00",
                    weightPrice:"62.00"
                }
            ]
        }
    }
}

</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .container{
        display: flex;
        align-items: flex-start;
        margin-top: 100px;
        justify-content: space-between;
    }
    .title{
        max-width: 250px;
        text-align: left;
        margin-left: 100px;
        
        p{
            color: $mamba;
            font-size: .5rem;
            margin-bottom: 20px;
        }
        h1{
            font-size: 1rem;
            color: $daisyBush;
        }
        button{margin-top: 30px;}

    }
    .purpleBtn{
        background-color: $daisyBush;
        color: $white;
        border-radius: 8px;
        padding: 10px 15px;
        border: none;
        cursor: pointer;
        font-size: .5rem;
        &:hover{    
        color: $daisyBush;
        background-color: rgb(236, 232, 243);
        }
    }   
</style>