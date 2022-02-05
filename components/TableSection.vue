<template>
  <div class="lg:px-20 px-4 py-2">
    <div class="filter justify-between flex">
      <div class="flex justify-between w-72">
        <div class="flex text-xs light text-purple rounded-lg p-2">
          All time
          <img class="w-2 h-2 mt-1 ml-1" src="../static/close.png" alt="" />
        </div>
        <div class="flex text-xs light text-purple rounded-lg p-2">
          US, AU, +4
          <img class="w-2 h-2 mt-1 ml-1" src="../static/close.png" alt="" />
        </div>
        <div class="flex text-xs border-2 rounded-lg p-2 px-3">
          <img class="w-3 h-2 mt-1 mr-1" src="../static/filter.png" alt="" />
          More filters
        </div>
      </div>
      <div class="mr-4 relative">
        <input
          type="text"
          placeholder="Search"
          class="pl-10 text-xs border-2 p-2 w-80 rounded-lg"
        />
        <img
          src="../static/search.png"
          class="absolute bottom-2 left-3"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.light {
  background-color: #f9f5ff;
}
</style>