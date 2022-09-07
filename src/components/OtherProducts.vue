<template>
    <div class="prodContainer">
        <section class="prodTitle">
            <h3>Find a freshly baked product perfect for you</h3>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A quo officia voluptatum. Cupiditate error, incidunt commodi asperiores rerum unde nisi autem perspiciatis! Hic ullam at libero natus. Hic, eum vel.</p>
            <button class="purpleBtn">Shop all products</button>
        </section>
        <section class="products">
            <div class="productpics">
                <OtherProductsComponent v-for="(product, index) in products" :key="index"
                :product="product.img"
                :productName="product.name"
                :productPrice="product.price"
                :productWeightPrice="product.weightPrice"
                />
            </div>
        </section>
    </div>
</template>

<script>
import OtherProductsComponent from "./OtherProductsComponent.vue"
export default {
    name: "OtherProducts",
    components: {OtherProductsComponent},
    data: function(){
        return{
            products:[
                {
                    img: "choco-chip-cookies-200x255.jpg",
                    name: "Choco Chip Cookies",
                    price: "19.00",
                    weightPrice: "39.00"
                },
                 {
                    img: "strawberry-jam-cookies-200x255.jpg",
                    name: "Srtawberry Jam Cookies",
                    price: "24.00",
                    weightPrice: "62.00"
                },
                 {
                    img: "strawberry-donut-200x255.jpg",
                    name: "Strawberry Donut",
                    price: "24.00",
                    weightPrice: "62.00"
                },
                 {
                    img: "perfect-macarons-200x255.jpg",
                    name: "Perfect Macarons",
                    price: "18.00",
                    weightPrice: "52.00"
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .prodContainer{
        display: flex;
        justify-content: space-between;
        margin-top: 100px;
    }

    .prodTitle{
        max-width: 350px;
        margin-left: 100px;
        text-align: left;
    }
    h3{color: $daisyBush;}
    p{
        color: $mamba;
        font-size: .5rem;
        margin-top: 30px;
    }

    .purpleBtn{
        background-color: $daisyBush;
        color: $white;
        border-radius: 8px;
        padding: 10px 15px;
        border: none;
        cursor: pointer;
        font-size: .5rem;
        margin-top: 50px;
        &:hover{    
        color: $daisyBush;
        background-color: rgb(236, 232, 243);
        }
    } 
    .productpics{
        display: flex;
        justify-content: space-around;
        margin-right: 100px
    }   
    

</style>