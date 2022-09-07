<template>
    <div class="container">
        <section class="title">
            <p>CORPORATE & WEDDINGS</p>
            <h3>Baking Special Moments</h3>
        </section>
        <section class="eventPics">
            <EventCard v-for="(item, index) in events" :key="index"
            :event="item.img"
            :eventHover="item.imgHover"
            :eventP="item.eventP"
            :eventH="item.eventH"
            />
        </section>
    </div>
</template>

<script>
import EventCard from "./EventCard.vue";
export default {
    name: "CorporateEvents",
    components: {EventCard},
    data: function(){
        return{
            events:[
                {
                    img:"corporate-bg.jpg",
                    imgHover:"corporate-hover-bg.jpg",
                    eventP:"INTERNATIONAL BAKERY",
                    eventH:"Corporate Events"
                },
                 {
                    img:"wedding-bg.jpg",
                    imgHover:"wedding-hover-bg.jpg",
                    eventP:"PRIVATE DINING HALL",
                    eventH:"Weddings & parties"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .container{
        margin-top: 100px;
        .title{
            text-align: center;
            p{
                color: $mamba;
                font-size:.5rem;
            }
            h3{
                font-size: 1rem;
                color: $daisyBush;
            }
        }
        .eventPics{
            display: flex;
            justify-content: space-around;
        }
    }
    

</style>