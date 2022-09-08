<template>
    <section class="instaPics">
        <div class="myPics">
            <InstaComponent v-for="(pic, index) in picsComponent" :key="index"
            :img="pic.img"
            :imgName="pic.imgName"
            />
        </div>
        <section class="instaTitle">
            <p>MADE FOR SHARING</p>
            <h3>Let's stay in touch</h3>
            <button class="purpleBtn"><i class="fa-brands fa-instagram"></i> Follow us</button>
        </section>
    </section>
</template>

<script>
import InstaComponent from "./InstaComponent.vue";
export default {
    name: "InstaPics",
    components: {InstaComponent},
    data: function (){
        return{
            picsComponent: [
                {
                    img:"social-1.jpg",
                    imgName: "social 1"
                },
                 {
                    img:"social-2.jpg",
                    imgName: "social 2"
                },
                 {
                    img:"social-3.jpg",
                    imgName: "social 3"
                },
                 {
                    img:"social-4.jpg",
                    imgName: "social 4"
                },
                 {
                    img:"social-5.jpg",
                    imgName: "social 5"
                },
                 {
                    img:"social-6.jpg",
                    imgName: "social 6"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .myPics{
        margin-top: 100px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
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
</style>