<template>
    <section class="myOrders">
        <div class="myText">
            <p>TRY OUR SEASONAL PRODUCTS</p>
            <h3>Order for pick-up or delivery to your home</h3>
            <button class="whiteBtn">Shop now</button>
        </div>
       
    </section>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

    .myOrders{
        margin-top: 100px;
        background-image: url("../assets/images/call-to-action-bg.jpg");
        background-size: cover;
        color: $white;
        height: 500px;

        .myText{
            text-align: left;
            line-height: 50px;
            margin-left: 100px;

            p{
                font-size: .7rem;
                color: $mamba;
            }

        }

    }
    .whiteBtn{
            color: $daisyBush;
            background-color: $white;
            border-radius: 8px;
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            font-size: .5rem;
            &:hover{
                background-color: $daisyBush;
                color: $white;
            }
        }
</style>