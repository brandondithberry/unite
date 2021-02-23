<template>
  <div class="rounded-md p-8 bg-gray-300 shadow-md">
    <h2 class="font-bold pb-3 font-display uppercase">Publish An Update</h2>
    <textarea
      class="block rounded-md p-3 text-black text-sm w-full box-border shadow-lg"
    ></textarea>
    <button
      class="p-3 mt-5 rounded-md bg-blue-600 text-white hover:bg-blue-500 shadow-lg mr-5 transition"
    >
      Publish
    </button>
    <button
      class="p-3 mt-5 rounded-md bg-gray-600 text-white hover:bg-gray-500 shadow-lg mr-5 transition"
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
      class="p-3 rounded-md bg-gray-600 text-white hover:bg-gray-500 shadow-lg transition"
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
import CalendarIcon from "@/components/graphics/CalendarIcon.vue";

export default {
  components: {
    CalendarIcon,
  },
};
</script>