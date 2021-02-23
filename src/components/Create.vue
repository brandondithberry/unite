<template>
  <div class="rounded-md p-8 bg-gray-900 text-white shadow-md">
    <h2 class="font-bold pb-3 font-display uppercase">Publish An Update</h2>
    <textarea
      class="block border-2 rounded-md p-3 text-black text-sm w-full box-border"
    ></textarea>
    <button
      class="p-3 mt-5 rounded-md bg-blue-500 text-white hover:bg-blue-400 shadow-xl mr-5"
    >
      Publish
    </button>
    <button
      class="p-3 mt-5 rounded-md bg-gray-500 text-white hover:bg-gray-400 shadow-xl mr-5"
    >
      <calendar-icon
        height="15"
        width="15"
        fill="white"
        class="inline align-top mt-1 mr-1"
      />
      New Event
    </button>
    <button
      class="p-3 rounded-md bg-gray-500 text-white hover:bg-gray-400 shadow-xl"
    >
      <calendar-icon
        height="15"
        width="15"
        fill="white"
        class="inline align-top mt-1 mr-1"
      />
      New Prayer
    </button>
  </div>
</template>

<script>
import CalendarIcon from "@/components/icons/CalendarIcon.vue";

export default {
  components: {
    CalendarIcon,
  },
};
</script>