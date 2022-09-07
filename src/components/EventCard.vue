<template>
    <div class="eventCard">
        <img :src="require('../assets/images/' + event)" :alt="eventName">
        <div class="eventHover">
            <img :src="require('../assets/images/' + eventHover)" :alt="eventNameHover">
            <div class="cardHover">
                <p>{{eventP}}</p>
                <h3>{{eventH}}</h3>
                <button class="purpleBtn">Explore more</button>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
    name: "EventCard",
    props: {
        event: String,
        eventName: String,
        eventHover: String,
        eventNameHover: String,
        eventP: String,
        eventH: String
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .eventCard{
        position: relative;
        width: 40%;
        cursor: pointer;
        margin-top: 50px;
        img{
            width: 600px;
            object-fit: cover;
        }
        &:hover .eventHover{display: inline-block;}
        .eventHover{
            position: absolute;
            display: none;
            
        }
        .cardHover{
            transform: translate(-50%, -50%);
            top: 50%;
            left: 50%;
            text-align: center;
            color: $white;
            width: 550px;
            p{font-size: .5rem;}
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
    }
</style>