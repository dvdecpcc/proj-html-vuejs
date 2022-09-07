<template>
  <div>
    <OurProductsMain/>
    <CorporateEvents/>
  </div>
</template>

<script>
import OurProductsMain from "./OurProductsMain.vue";
import CorporateEvents from "./CorporateEvents.vue";

export default {
  name: "MyMain",
  components: {
    OurProductsMain,
    CorporateEvents,
  }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

</style>