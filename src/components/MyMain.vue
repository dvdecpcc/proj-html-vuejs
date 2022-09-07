<template>
  <div>
    <OurProductsMain/>
    <CorporateEvents/>
    <OtherProducts/>
  </div>
</template>

<script>
import OurProductsMain from "./OurProductsMain.vue";
import CorporateEvents from "./CorporateEvents.vue";
import OtherProducts from "./OtherProducts.vue";

export default {
  name: "MyMain",
  components: {
    OurProductsMain,
    CorporateEvents,
    OtherProducts
  }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

</style>