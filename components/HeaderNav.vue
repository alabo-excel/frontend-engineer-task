<template>
  <div class="">
    <div class="flex lg:px-20 px-4 p-2 justify-between border-b-2">
      <div class="flex">
        <img class="lg:w-32 h-8 mt-1" src="../static/Logo.png" alt="" />
        <div class="px-8 text-sm flex mt-1 nav">
          <div class="mx-2 pt-1">Home</div>
          <div class="px-4 pt-1 active rounded-lg">Dashboard</div>
          <div class="mx-4 pt-1">Projects</div>
          <div class="mx-4 pt-1">Tasks</div>
          <div class="mx-4 pt-1">Reporting</div>
          <div class="mx-4 pt-1">Users</div>
        </div>
      </div>
      <div class="flex w-80 justify-evenly nav">
        <div class="flex p-1 px-3 border-2 rounded-lg text-xs">
          <img class="mr-2 w-3 h-4 mt-1" src="../static/upgrade.png" alt="" />
          <div class="p-1">Upgrade now</div>
        </div>
        <div class="mt-2">
          <img src="../static/settings.png" alt="" />
        </div>
        <div class="mt-2">
          <img src="../static/notification.png" alt="" />
        </div>
        <div>
          <img class="w-8 mt-1" src="../static/Avatar.png" alt="" />
        </div>
      </div>
      <div class="bar py-3">
        <img class="w-4" src="../static/hamburger.png" alt="" />
      </div>
    </div>
    <div class="flex px-20 p-3 justify-between border-b-2 nav">
      <div class="flex text-sm pt-1">
        <div class="px-4 active rounded-lg pt-1">Overview</div>
        <div class="mx-4 pt-1">Notification</div>
        <div class="mx-4 pt-1">Analytics</div>
        <div class="mx-4 pt-1">Saved reports</div>
        <div class="mx-4 pt-1">Trade history</div>
        <div class="mx-4 pt-1">User reports</div>
      </div>
      <div class="mr-6 relative">
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

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap");
div {
  font-family: "Inter"!important;
  color: #344054;
  font-weight: normal !important;
}
.border-2 {
  border-width: 1px !important;
  border-color: #d0d5dd;
}
.border-b-2 {
  border-bottom: 1px #d0d5dd solid;
}
.bg-purple {
  background-color: #7f56d9;
}
.text-purple {
  color: #6941C6;
}
.bar {
  display: none;
}
.active {
  background-color: #f9fafb;
}
@media (max-width: 600px) {
  .bar {
    display: block;
  }
  .nav {
    display: none;
  }
}
</style>