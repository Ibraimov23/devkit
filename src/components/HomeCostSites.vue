<template lang="pug">
section(class="cost-sites" id="stoimost")
  h2(class="capitalize font-bold text-center") стоимость сайтов
  home-cost-sites-card
</template>

<script>
import HomeCostSitesCard from "./HomeCostSitesCard";

export default {
  name: "HomeCostSites",
  components: { HomeCostSitesCard },
};
</script>

<style scoped lang="scss">
h2 {
  font-size: 50px;
  margin-bottom: 55px;
}
</style>
