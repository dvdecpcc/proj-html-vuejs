<template>
  <div class="card">
    <img :src="require('../assets/images/' + item)" alt="itemName">
    <div class="infos">
        <h3>{{itemName}}</h3>
        <p>{{itemType}}</p>
        <h3>${{itemPrice}}  ${{itemWeightPrice}}</h3>
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
        &:hover .infos{
            display: block;
        }
        img{width: 100%;}
        .infos{
            position: absolute;
            display: none;
            background-color: rgba(0,0,0,.5);
            top: 50%;
            left: 50%;
            color: $white;
            text-align: center;
        }
    }

</style>