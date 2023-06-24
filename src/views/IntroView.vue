<template>
  <div>
    <ContTitle title="INTRO" />
    <IntroSlider />
    <IntroCont />
    <IntroSite />
  </div>
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import IntroSlider from "@/components/intro/IntroSlider.vue";
import IntroCont from "@/components/intro/IntroCont.vue";
import IntroSite from "@/components/intro/IntroSite.vue";

export default {
  components: {
    ContTitle,
    IntroSlider,
    IntroCont,
    IntroSite,
  },
};
</script>
