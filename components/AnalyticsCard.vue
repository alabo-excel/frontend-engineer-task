<template>
  <div class="border-2 p-4 lg:w-1/3 my-2 lg:mr-4 rounded-lg">
    <div class="flex justify-between">
      <div class="text-black capitalize lg:text-base text-sm">{{ analytics[index].title }}</div>
      <div>
        <img class="w-1 h-3 mt-2" src="../static/Icon.png" alt="" />
      </div>
    </div>
    <div class="flex justify-between relative">
      <div>
        <div class="text-black lg:text-3xl text-xl my-5">
          {{ analytics[index].number }}
        </div>
        <div class="text-xs flex">
          <img
            v-if="analytics[index].percent < 20"
            class="w-3 h-3 mr-2"
            src="../static/dwn.png"
            alt=""
          />
          <img v-else class="w-3 h-3 mr-2" src="../static/up.png" alt="" />
          <div
            class="px-1"
            :class="[
              analytics[index].percent < 20 ? 'text-red-600' : 'text-green-600',
            ]"
          >
            {{ analytics[index].percent }}%
          </div>
          vs last month
        </div>
      </div>
      <div class="">
        <img
          v-if="analytics[index].percent < 20"
          class="absolute bottom-0 right-0 lg:w-auto w-20"
          src="../static/red.png"
          alt=""
        />
        <img
          v-else
          class="absolute bottom-0 right-0 lg:w-auto w-20"
          src="../static/green.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    analytics: Array,
    index: Number,
  },
  mounted() {
    // console.log(analytics);
  },
};
</script>