<template>
  <div>
    <div class="lg:flex justify-between lg:mx-20 mx-4">
      <AnalyticsCard :analytics="analytics" :index="index" v-for="(analytic, index) in analytics" :key="index" />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      analytics: [
        {
          title: "total customers",
          number: "2,420",
          percent: 40,
        },
        {
          title: "members",
          number: "1,210",
          percent: 10,
        },
        {
          title: "active now",
          number: "316",
          percent: 20,
        },
      ],
    };
  },
};
</script>