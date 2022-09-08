<template>
  <div>
    <OurProductsMain/>
    <CorporateEvents/>
    <OtherProducts/>
    <StoreProcess/>
    <StoreLoc/>
  </div>
</template>

<script>
import OurProductsMain from "./OurProductsMain.vue";
import CorporateEvents from "./CorporateEvents.vue";
import OtherProducts from "./OtherProducts.vue";
import StoreProcess from "./StoreProcess.vue";
import StoreLoc from "./StoreLoc.vue";

export default {
  name: "MyMain",
  components: {
    OurProductsMain,
    CorporateEvents,
    OtherProducts,
    StoreProcess,
    StoreLoc
  }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

</style>