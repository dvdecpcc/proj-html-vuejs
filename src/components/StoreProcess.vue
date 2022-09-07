<template>
    <div class="processContainer">
        <ProcessComponent v-for="text in descriptionText" :key="text.number"
        :processPic="text.img"
        :number="text.number"
        :processName="text.name"
        :processP="text.p"
        :processDetail="text.detail"
        />
        <section class="founder">
            <p>DON'T JUST TAKE OUR WORD FOR IT</p>
            <h3>"Finally found an alternative to mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity"</h3>
            <p>Rachel Cooper, Founder</p>
        </section>
    </div>
</template>

<script>
import ProcessComponent from "./ProcessComponent.vue";
export default {
    name: "StoreProcess",
    components: {ProcessComponent},
    data: function(){
        return{
            descriptionText:[
                {
                 img:"bakery-process-1.jpg",
                 number:"01",  
                 name:"Tell us what you have in mind",
                 p:"MANUAL INGREDIENTS SELECTION",
                 detail:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."   
                },
                {
                 img:"bakery-process-2.jpg",
                 number:"02",  
                 name:"We start baking",
                 p:"SWEET & DELICIOUS",
                 detail:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."   
                },
                {
                 img:"bakery-process-3.jpg",
                 number:"03",  
                 name:"Delivered to your home",
                 p:"BAKED TO ORDER & GIFT WRAPPED",
                 detail:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."   
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .processContainer{
        margin-top: 100px;
    }
</style>