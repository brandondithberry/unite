<template>
  <div
    v-for="post in posts"
    :key="post.id"
    class="grid p-8 bg-gray-100 rounded-md shadow-md gap-5 grid-cols-12"
  >
    <div class="grid 2xl:col-span-9 col-span-full">
      <h3>
        <span class="font-display">{{ post.author }}</span> - Published on
        {{ post.date }}
      </h3>
      <h5 class="text-gray-500">{{ post.role }} • {{ post.church }}</h5>
      <p class="my-4 py-4 border-t border-b border-gray-300">{{ post.body }}</p>
      <h6 class="text-blue-500">
        <b>Category:</b> {{ post.category }}<br /><b>Tags:</b> {{ post.tags }}
      </h6>
    </div>
    <div class="grid 2xl:col-span-3 col-span-full">
      <img
        :src="post.photo"
        width="250"
        height="250"
        class="object-cover rounded-md"
      />
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      posts: [
        {
          id: 1,
          photo:
            "https://www.alexslemonade.org/sites/default/files/styles/blog_full/public/cooper_1.jpg?itok=zAVQQBKP",
          author: "Kelley Wright",
          role: "Worship Director",
          church: "Vineyard Church Westbrook",
          category: "Praise Report",
          date: "March 10, 2021",
          body:
            "I'm so happy to announce that my neice is cancer free! Praise God!",
          tags: "praise, jesus",
        },
        {
          id: 2,
          photo:
            "https://images.genius.com/c2ea28773acc1efc0b8d5d33e116045e.1000x1000x1.jpg",
          author: "John Daniels",
          role: "Discipleship Pastor",
          church: "Cornerstone Maine",
          category: "Worship",
          date: "March 9, 2021",
          body: "Been listening to the new Red Rocks Album, it's phenominal.",
          tags: "praise, jesus",
        },
        {
          id: 2,
          photo:
            "https://images.genius.com/c2ea28773acc1efc0b8d5d33e116045e.1000x1000x1.jpg",
          author: "John Daniels",
          role: "Discipleship Pastor",
          church: "Cornerstone Maine",
          category: "Worship",
          date: "March 9, 2021",
          body: "Been listening to the new Red Rocks Album, it's phenominal.",
          tags: "praise, jesus",
        },
        {
          id: 2,
          photo:
            "https://images.genius.com/c2ea28773acc1efc0b8d5d33e116045e.1000x1000x1.jpg",
          author: "John Daniels",
          role: "Discipleship Pastor",
          church: "Cornerstone Maine",
          category: "Worship",
          date: "March 9, 2021",
          body: "Been listening to the new Red Rocks Album, it's phenominal.",
          tags: "praise, jesus",
        },
      ],
    };
  },
};
</script>