<template>
  <div>
    <header>
      <TopBar />
    </header>

    <div class="container w-full grid grid-flow-col grid-cols-12 mx-auto">
      <div class="grid col-span-9">
        <section id="create" class="rounded-md m-5 p-8 bg-gray-900 text-white">
          <Create />
        </section>

        <section id="posts">
          <Posts />
        </section>
      </div>

      <div class="grid col-span-3">
        <Sidebar />
      </div>
    </div>
  </div>
</template>

<script>
import TopBar from "./components/TopBar.vue";
import Create from "./components/Create.vue";
import Posts from "./components/Posts.vue";
import Sidebar from "./components/Sidebar.vue";
import "@/assets/css/tailwind.css";

export default {
  name: "App",
  components: {
    TopBar,
    Create,
    Posts,
    Sidebar,
  },
};
</script>