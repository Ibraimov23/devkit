<template lang="pug">
div
  home-header
  home-last-projects
  home-cost-sites
  home-our-approach
  home-steps
  home-contact-us
</template>

<script>
import HomeHeader from "@/components/HomeHeader";
import HomeLastProjects from "@/components/HomeLastProjects";
import HomeCostSites from "@/components/HomeCostSites";
import HomeOurApproach from "@/components/HomeOurApproach";
import HomeSteps from "@/components/HomeSteps";
import HomeContactUs from "@/components/HomeContactUs";

export default {
  name: "HomeView",
  components: {
    HomeHeader,
    HomeLastProjects,
    HomeCostSites,
    HomeOurApproach,
    HomeSteps,
    HomeContactUs,
  },
};
</script>
