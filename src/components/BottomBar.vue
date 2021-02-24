<template>
  <div
    class="flex flex-wrap col-span-full bg-gray-900 bg-opacity-90 text-gray-100 tracking-wide shadow-md sticky bottom-0 md:hidden"
    style="backdrop-filter: blur(5px)"
  >
    <div class="w-full px-4">
      <nav
        class="relative flex flex-wrap items-center justify-between px-2 py-3"
      >
        <ul class="flex flex-row list-none col-span-full m-auto">
          <li class="nav-item">
            <a class="pr-7 py-2 flex items-center" href="#">
              <home-icon height="50" width="50" class="active" />
            </a>
          </li>
          <li class="nav-item">
            <a class="pr-7 py-2 flex items-center" href="#">
              <prayer-icon height="50" width="50" />
            </a>
          </li>
          <li class="nav-item">
            <a class="pr-7 py-2 flex items-center" href="#">
              <inbox-icon height="50" width="50" />
            </a>
          </li>
          <li class="nav-item">
            <a class="pr-7 py-2 flex items-center" href="#">
              <calendar-icon height="50" width="50" />
            </a>
          </li>
          <li class="nav-item">
            <a class="py-2 flex items-center" href="https://my.uniteco.app">
              <settings-icon height="50" width="50" />
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
import HomeIcon from "@/components/graphics/HomeIcon.vue";
import InboxIcon from "@/components/graphics/InboxIcon.vue";
import CalendarIcon from "@/components/graphics/CalendarIcon.vue";
import PrayerIcon from "@/components/graphics/PrayerIcon.vue";
import SettingsIcon from "@/components/graphics/SettingsIcon.vue";

export default {
  data: function () {
    return {};
  },
  components: {
    HomeIcon,
    InboxIcon,
    CalendarIcon,
    PrayerIcon,
    SettingsIcon,
  },
};
</script>

<style>
.nav-item svg {
  fill: #fff;
  stroke: #fff;
  stroke-opacity: 1;
  fill-opacity: 1;
}
.nav-item a:hover svg,
.nav-item svg.active {
  fill-opacity: 0;
}
.nav-item a {
  transition: 0.4s ease !important;
}
svg:not(:root) {
  overflow: visible !important;
}
</style>