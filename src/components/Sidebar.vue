<template>
  <div class="grid col-span-4 gap-6">
    <div class="grid rounded-md p-8 bg-blue-100 leading-loose shadow-md">
      <h4 class="font-display uppercase text-md">Messages</h4>
      <ul class="text-sm">
        <li
          v-for="message in messages.slice(0, 4)"
          :key="message.id"
          class="border-2 border-blue-300 p-3 mt-5 rounded-md flex justify-between"
        >
          <p>
            <span v-if="message.body.length<50">{{ message.body }}</span>
            <span v-else>{{ message.body.substring(0,50) + "..."}}</span><br />
            <b
              >{{ message.sender }} | {{ message.date }} -
              {{ message.time }}</b
            >
          </p>
          <options-icon
            width="15"
            height="15"
            class="opacity-30 hover:opacity-100 cursor-pointer"
          ></options-icon>
        </li>
      </ul>
    </div>
    <div class="grid rounded-md p-8 bg-yellow-100 leading-loose shadow-md">
      <h4 class="font-display uppercase text-md">Prayer Reminders</h4>
      <ul class="text-sm">
        <li
          v-for="prayer in prayers.slice(0, 4)"
          :key="prayer.id"
          class="border-b-2 border-yellow-300 pb-2 mt-4 flex justify-between"
        >
          <p>
            {{ prayer.title }} | <b>{{ prayer.date }} at {{ prayer.time }}</b>
          </p>
          <check-icon
            width="15"
            height="15"
            class="opacity-30 hover:opacity-100 cursor-pointer"
          ></check-icon>
        </li>
      </ul>
    </div>
    <div class="grid rounded-md p-8 bg-purple-100 leading-loose shadow-md">
      <h4 class="font-display uppercase text-md mb-4">Upcoming Events</h4>
      <ul class="text-sm grid grid-cols-1 xl:grid-cols-2 gap-3">
        <li
          v-for="event in events.slice(0, 4)"
          :key="event.id"
          class="border-2 border-purple-300 pb-2 rounded-md p-3"
        >
          <p>
            <b>{{ event.title }}</b
            ><br />{{ event.category }}<br />{{ event.location }}<br /><i
              ><b>{{ event.date }} - {{ event.time }}</b></i
            >
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import CheckIcon from "@/components/icons/CheckIcon.vue";
import OptionsIcon from "@/components/icons/OptionsIcon.vue";

export default {
  data: function () {
    return {
      messages: [
        {
          id: 1,
          body: "Hey, don't forget to pray for Amy today.",
          sender: "Eric B.",
          date: "3/7",
          time: "3pm",
        },
        {
          id: 2,
          body: "Want to grab lunch next week?",
          sender: "Steve T.",
          date: "3/5",
          time: "1pm",
        },
        {
          id: 3,
          body: "Hey! what's up?",
          sender: "Emma W.",
          date: "3/5",
          time: "10am",
        },
        {
          id: 4,
          body: "Just saw the new sermon. Amazing!",
          sender: "Tom K.",
          date: "3/5",
          time: "9am",
        },
      ],
      prayers: [
        { id: 1, title: "Pray for Amy", date: "Today", time: "3pm" },
        { id: 2, title: "Pray for Tom", date: "Today", time: "3pm" },
      ],
      events: [
        {
          id: 1,
          title: "On The Throne",
          category: "Worship Night",
          location: "Harvest Chapel",
          date: "March 7",
          time: "5pm",
        },
        {
          id: 2,
          title: "New Life",
          category: "Worship Night",
          location: "East Auburn Baptist",
          date: "March 10",
          time: "5pm",
        },
        {
          id: 3,
          title: "As You Are",
          category: "Worship Night",
          location: "The Ark Huntsville",
          date: "March 20",
          time: "5pm",
        },
        {
          id: 4,
          title: "Greater Things",
          category: "Worship Night",
          location: "The Ark Huntsville",
          date: "March 30",
          time: "5pm",
        },
      ],
    };
  },
  components: {
    CheckIcon,
    OptionsIcon,
  },
};
</script>