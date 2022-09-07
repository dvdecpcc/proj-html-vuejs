<template>
    <section class="processContainer">
        <div class="storeProc">
            <div class="processImg">
                <img :src="require('../assets/images/' + processPic)">
            </div>
            <div class="properties">
                <div class="imageTitle">
                    <h3>{{processName}}</h3>
                    <h3 class="number">{{number}}</h3>
                </div>
                <div class="paragraph">
                    <p>{{processP}}</p>
                    <p>{{processDetail}}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "ProcessComponent",
    props: {
        processPic: String,
        number: String,
        processName: String,
        processP: String,
        processDetail: String
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";
    .processContainer{
        position: relative;

        img{
            width: 100%;
            object-fit: cover;
        }
        .properties{
            background-color: rgba(0,0,0,.6);
            color: $white;
            top: 0;
            left: 0;
            position: absolute;
            padding: 30px;
            width: 100%;
            height: 100%;

            .imageTitle{
                display: flex;
                justify-content: space-between;
            }
            h3{
                font-size: 1rem;
                float: left;
            }
            .number{
                font-size: 1rem;
                text-align: end;
            }
            .paragraph{
                font-size: .7rem;
                color: $mamba;
            }
        }

    }

</style>