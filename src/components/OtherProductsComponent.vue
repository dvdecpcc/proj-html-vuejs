<template>
    <div class="otherProducts">
        <div class="productPics">
            <img :src="require('../assets/images/' + product)" alt="productName">
            <p>SELECT OPTIONS / QUICK VIEW</p>
        </div>
        <div class="productsInfo">
            <h4>{{productName}}</h4>
            <p>${{productPrice}} - ${{productWeightPrice}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "OtherProductsComponent",
    props: {
        product: String,
        productName: String,
        productPrice: String,
        productWeightPrice: String
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .otherProducts{cursor: pointer;}    
    p:hover{display: block;}
    .productPics{
        width: 100%;
        position: relative;

        img{
            margin: 15px;
        }
    }
    p{
        display: none;
        background-color: rgba(0, 0, 0, .5);
        transform: translate(-50%, -50%);
        top: 50%;
        left: 50%;
        width: 100%;
        height: 100%;
        text-align: center;
    }
    h4{color: $daisyBush;}

    .productsInfo p{
        font-size: .5rem;
        color: $mamba
    }
    

</style>