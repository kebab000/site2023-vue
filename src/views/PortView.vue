<template>
  <div>
    <ContTitle title="PORTFOLIO" />
    <PortSlider />
    <PortCont />
  </div>
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import PortSlider from "@/components/port/PortSlider.vue";
import PortCont from "@/components/port/PortCont.vue";

export default {
  components: {
    ContTitle,
    PortSlider,
    PortCont,
  },
};
</script>
