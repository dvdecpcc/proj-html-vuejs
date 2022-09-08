<template>
    <div class="storesLocations">
        <section class="heading">
            <p>LOCATIONS</p>
            <h3>Visit our Bakeries</h3>
        </section>
        <section class="locationsinfo">
            <LocComponent v-for="(info, index) in infos" :key="index"
            :pic="info.pic"
            :place="info.place"
            :phoneNumber="info.phoneNumber"
            :timing="info.timing"
            />
        </section>
    </div>
</template>

<script>
import LocComponent from "./LocComponent.vue";
export default {
    name: "StoreLoc",
    components: {LocComponent},
    data: function (){
        return{
            infos: [
               {
                pic:"new-york-bk-800x530.jpg",
                place:"New York",
                phoneNumber:"1.800.458.556",
                timing:"9:00 AM - 6:00 PM"
               },
               {
                pic:"london-bk-800x530.jpg",
                place:"London",
                phoneNumber:"1.800.458.556",
                timing:"9:00 AM - 6:00 PM"
               }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .storesLocations{

        .heading{
            text-align: center;
            margin-top: 100px;
        }
        .locationsinfo{
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 50px;
        }
    }
</style>