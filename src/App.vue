<template>
  <div>
    <TopBar />

    <div
      class="container w-full grid grid-flow-col grid-cols-12 mx-auto items-start gap-10 p-10"
    >
      <Content />

      <Sidebar />
    </div>
  </div>
</template>

<script>
import TopBar from "./components/TopBar.vue";
import Content from "./components/Content.vue";
import Sidebar from "./components/Sidebar.vue";
import "@/assets/css/tailwind.css";

export default {
  name: "App",
  components: {
    TopBar,
    Content,
    Sidebar,
  },
};
</script>