<template>
  <div class="flex flex-wrap bg-gray-900 bg-opacity-90 text-gray-100 tracking-wide shadow-md sticky top-0" style="backdrop-filter: blur(5px);">
    <div class="w-full px-4">
      <nav
        class="relative flex flex-wrap items-center justify-between px-2 py-3"
      >
        <div
          class="container px-4 mx-auto flex flex-wrap items-center justify-between"
        >
          <div
            class="w-full relative flex justify-between sm:w-auto sm:static sm:block sm:justify-start"
          >
            <a
              class="text-xl font-bold leading-relaxed inline-block whitespace-no-wrap uppercase font-display"
              href="#"
            >
              <logo-light width="150" />
            </a>
          </div>
          <ul class="flex flex-row list-none ">
            <li class="nav-item">
              <a class="pr-7 py-2 flex items-center" href="#">
                <home-icon height="20" width="20" class="active" />
              </a>
            </li>
            <li class="nav-item">
              <a class="pr-7 py-2 flex items-center" href="#">
                <prayer-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="pr-7 py-2 flex items-center" href="#">
                <inbox-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="pr-7 py-2 flex items-center" href="#">
                <calendar-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="py-2 flex items-center" href="https://my.uniteco.app">
                <settings-icon height="20" width="20" />
              </a>
            </li>
          </ul>
        </div>
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
import LogoLight from "@/components/graphics/LogoLight.vue";

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
    LogoLight,
    
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