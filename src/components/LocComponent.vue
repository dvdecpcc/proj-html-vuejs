<template>
    <div class="storesContainer">
        <section class="imgSection">
            <img :src="require('../assets/images/' + pic)">
        </section>
        <section class="stores">
            <h3>{{place}}</h3>
            <div class="contacts">
                <p>CALL US<span>{{phoneNumber}}</span></p>
                <p>OPEN ALL WEEK<span>{{timing}}</span></p>
                <button class="whiteBtn">View Map</button>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    name:"LocComponent",
    props: {
        pic: String,
        place: String,
        phoneNumber: String,
        timing: String
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

    .storesContainer{
        
        &:nth-child(1){background-color: $newYork;}
        &:nth-child(2){background-color: $london;}
        img{width: 100%;}
        h3{color: $daisyBush;}
        .contacts{
            display: flex;
            justify-content: space space-around;
            align-items: center;

            p{
            font-size: .5rem;
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