<template>
    <div class="instaPic">
        <img :src="require('../assets/images/' + img)" alt="imgName">
    </div>
</template>

<script>
export default {
    name: "InstaComponent",
    props: {
        img: String,
        imgName: String
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .instaPic{
        width: calc(100% / 4 - 10px);
        img{
            width: 100%;
        }
    }

</style>