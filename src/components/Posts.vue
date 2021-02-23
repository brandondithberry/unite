<template>
  <div
    v-for="post in posts"
    :key="post._id"
    class="grid p-8 bg-gray-100 rounded-md shadow-md gap-5 grid-cols-12"
  >
    <div class="grid 2xl:col-span-9 col-span-full">
      <h3>
        <span class="font-display" v-for="user in users" :key="user._id">{{
          user.name
        }}</span>
        - Published on
        <span id="timestamp">{{ post._modified }}</span>
      </h3>
      <h5 class="text-gray-500" v-for="profile in profiles" :key="profile._by">
        {{ profile.role }} {{ profile.church }}
      </h5>
      <p class="my-4 py-4 border-t border-b border-gray-300">
        {{ post.body }}
      </p>
      <h6 class="text-blue-500"><b>Category:</b> {{ post.category }}</h6>
      <h6 class="text-blue-500 mt-4">
        <b>Tags:</b>
        <a
          href="#"
          class="py-1 px-2 m-1 border-2 border-blue-500 hover:bg-blue-200 rounded-md transition"
          v-for="tag in post.tags"
          :key="tag._id"
          >{{ tag }}</a
        >
      </h6>
    </div>
  </div>
</template>

<script>
const posturl =
  "//my.uniteco.app/api/collections/get/posts?token=693278b23048cc329c391feac0e761";
const listusers =
  "//my.uniteco.app/api/cockpit/listUsers?token=693278b23048cc329c391feac0e761";
const profileurl =
  "//my.uniteco.app/api/singletons/get/profile?token=693278b23048cc329c391feac0e761";

export default {
  data: function () {
    return {
      posts: [],
      users: [],
      profiles: [],
    };
  },
  mounted() {
    fetch(posturl)
      .then((data) => data.json())
      .then((data) => {
        this.posts = data.entries;
        console.log(data.entries);
      });

    fetch(listusers)
      .then((user) => user.json())
      .then((user) => {
        this.users = user;
        console.log(user);
      });

    fetch(profileurl)
      .then((data) => data.json())
      .then((data) => {
        this.profiles = data;
        console.log(data);
      });
  },
};
</script>