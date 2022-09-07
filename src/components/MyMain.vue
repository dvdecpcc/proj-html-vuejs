<template>
  <div>
    <OurProductsMain/>
    <CorporateEvents/>
    <OtherProducts/>
    <StoreProcess/>
  </div>
</template>

<script>
import OurProductsMain from "./OurProductsMain.vue";
import CorporateEvents from "./CorporateEvents.vue";
import OtherProducts from "./OtherProducts.vue";
import StoreProcess from "./StoreProcess.vue";

export default {
  name: "MyMain",
  components: {
    OurProductsMain,
    CorporateEvents,
    OtherProducts,
    StoreProcess
  }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

</style>