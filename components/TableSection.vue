<template>
  <div class="lg:px-20 px-4 py-4">
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
    <div
      class="lg:mr-4 mt-5 border-collapse border border-slate-700 rounded-lg "
    >
      <table class="w-full rounded-lg text-sm">
        <thead>
          <tr class="border-b-2 text-left px-4">
            <th class="p-2 flex">
              Company
              <img class="w-2 h-3 mt-1 mx-1" src="../static/down.png" alt="" />
            </th>
            <th>License use</th>
            <th>Status</th>
            <th>Users</th>
            <th class="w-80">About</th>
          </tr>
        </thead>
        <tbody>
          <tr
            :class="company.bg == true ? 'bg' : ''"
            v-for="(company, index) in companies"
            :key="index"
          >
            <td class="p-3 lg:px-4">
              <div class="flex">
                <div class="pt-3">
                  <label class="container">
                    <input type="checkbox" checked="checked" />
                    <span class="checkmark"></span>
                  </label>
                </div>
                <div class="mx-2">
                  <img class="w-10" src="../static/catalog.png" alt="" />
                </div>
                <div>
                  <div class="text-black capitalize">{{ company.name }}</div>
                  <div class="text-xs">{{ company.website }}</div>
                </div>
              </div>
            </td>
            <td>
              <div class="w-full rounded-lg bg-gray-200 h-1" style="width: 85%">
                <div class="bg-purple rounded-lg h-1" style="width: 45%"></div>
              </div>
            </td>
            <td>
              <div
                :class="company.status"
                class="rounded-lg p-1 capitalize text-xs w-16"
              >
                {{ company.status }}
              </div>
            </td>
            <td>
              <div class="flex">
                <img
                  class="w-5 h-5 -ml-1 border-1 rounded-lg border-white"
                  src="../static/Avatar.png"
                  alt=""
                />
                <img
                  class="w-5 h-5 -ml-1 border-1 rounded-lg border-white"
                  src="../static/Avatar.png"
                  alt=""
                />
                <img
                  class="w-5 h-5 -ml-1 border-1 rounded-lg border-white"
                  src="../static/Avatar.png"
                  alt=""
                /><img
                  class="w-5 h-5 -ml-1 border-1 rounded-lg border-white"
                  src="../static/Avatar.png"
                  alt=""
                /><img
                  class="w-5 h-5 -ml-1 border-1 rounded-lg border-white"
                  src="../static/Avatar.png"
                  alt=""
                />
                <div
                  class="
                    w-5
                    h-5
                    -ml-1
                    border-1
                    rounded-lg
                    border-white
                    text-xs text-purple
                    light
                  "
                >
                  +8
                </div>
              </div>
            </td>
            <td>
              <div class="flex">
                <div>
                  <div class="text-black">
                    {{ company.about }}
                  </div>
                  <div class="text-xs">{{ company.sub }}</div>
                </div>
                <div class="flex pt-3">
                  <img class="w-4 h-4 ml-5" src="../static/trash.png" alt="" />
                  <img class="w-4 h-4 ml-5" src="../static/pen.png" alt="" />
                </div>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
      <div class="flex justify-between w-full">
        <div class="mx-3 m-2">
          <input
            type="button"
            value="Previous"
            class="p-2 border-2 bg-white text-xs rounded-lg"
          />
          <input
            type="button"
            value="Next"
            class="p-2 border-2 bg-white text-xs rounded-lg mx-4"
          />
        </div>
        <div class="text-xs p-3">Page 1 of 10</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      companies: [
        {
          name: "catalog",
          website: "catalogapp.io",
          lisence: "40",
          status: "customer",
          about: "Content curating app",
          sub: "Brings all your news into one place",
          bg: true,
        },
        {
          name: "catalog",
          website: "catalogapp.io",
          lisence: "20",
          status: "churned",
          about: "Content curating app",
          sub: "Brings all your news into one place",
          bg: false,
        },
        {
          name: "command",
          website: "catalogapp.io",
          lisence: "20",
          status: "customer",
          about: "Content curating app",
          sub: "Brings all your news into one place",
          bg: true,
        },
        {
          name: "Hourglass",
          website: "catalogapp.io",
          lisence: "20",
          status: "churned",
          about: "Content curating app",
          sub: "Brings all your news into one place",
          bg: false,
        },
        {
          name: "command",
          website: "catalogapp.io",
          lisence: "20",
          status: "customer",
          about: "Content curating app",
          sub: "Brings all your news into one place",
          bg: true,
        },
      ],
    };
  },
};
</script>
<style scoped>
.light {
  background-color: #f9f5ff;
}
.border-1 {
  border-width: 1px !important;
}
.customer {
  color: #027a48;
  background-color: #ecfdf3;
}
.bg {
  background-color: #f9fafb;
}
.churned {
  color: #344054;
  background-color: #f2f4f7;
}
/* The container */
.container {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default checkbox */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

/* Create a custom checkbox */
.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 15px;
  width: 15px;
  background-color: #fff;
  border: 1px solid #7f56d9;
}

/* On mouse-over, add a grey background color */
.container:hover input ~ .checkmark {
  background-color: #ccc;
}

/* When the checkbox is checked, add a blue background */
.container input:checked ~ .checkmark {
  background-color: #f9f5ff;
}

/* Create the checkmark/indicator (hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the checkmark when checked */
.container input:checked ~ .checkmark:after {
  display: block;
}

/* Style the checkmark/indicator */
.container .checkmark:after {
  left: 4px;
  top: 0px;
  width: 5px;
  height: 10px;
  border: solid #7f56d9;
  border-width: 0 1px 1px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>