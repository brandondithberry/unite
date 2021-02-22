<template>
  <div class="flex flex-wrap bg-gray-100 text-gray-900 tracking-wide">
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
              class="text-lg font-bold leading-relaxed inline-block whitespace-no-wrap uppercase font-display"
              href="#"
            >
              UNITE
            </a>
          </div>
          <ul class="flex flex-col sm:flex-row list-none ml-auto">
            <li class="nav-item">
              <a class="pr-6 py-2 flex items-center hover:opacity-50" href="#">
                <home-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="pr-6 py-2 flex items-center hover:opacity-50" href="#">
                <inbox-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="pr-6 py-2 flex items-center hover:opacity-50" href="#">
                <calendar-icon height="20" width="20" />
              </a>
            </li>
            <li class="nav-item">
              <a class="py-2 flex items-center hover:opacity-50" href="#">
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
import HomeIcon from "@/components/icons/HomeIcon.vue";
import InboxIcon from "@/components/icons/InboxIcon.vue";
import CalendarIcon from "@/components/icons/CalendarIcon.vue";
import SettingsIcon from "@/components/icons/SettingsIcon.vue";

export default {
  data: function () {
    return {};
  },
  components: {
    HomeIcon,
    InboxIcon,
    CalendarIcon,
    SettingsIcon,
  },
};
</script>

<style>
svg:not(:root) {
  overflow: visible !important;
}
</style>