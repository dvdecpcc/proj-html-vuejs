<template>
  <div class="card">
    <img :src="require('../assets/images/' + item)" alt="itemName">
    <div class="infos">
        <h3>{{itemName}}</h3>
        <p>{{itemType}}</p>
        <h3>${{itemPrice}}    ${{itemWeightPrice}}</h3>
    </div>
  </div>
</template>

<script>
export default {
    name: "ourProducts",
    props: {
        item: String,
        itemName: String,
        itemType: String,
        itemPrice: String,
        itemWeightPrice: String,
    },
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .card{
        position: relative;
        cursor: pointer;
        display: inline-block;
        margin: 20px;
        &:hover .infos{
            display: block;
        }
        img{width: 300px;}
        .infos{
            position: absolute;
            display: none;
            background-color: rgba(0,0,0,.5);
            top: 50%;
            left: 50%;
            color: $white;
            text-align: center;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 100%;
            padding-top: 150px;
            line-height: 40px;

            h3{font-size: .9rem;}
            p{font-size: .5rem;}
        }
    }

</style>