<template>
  <div class="grid xl:col-span-8 col-span-full gap-10">
    <Create />

    <Posts />
  </div>
</template>

<script>
import Create from "@/components/Create.vue";
import Posts from "@/components/Posts.vue";

export default {
    components: {
        Create,
        Posts
    }
}
</script>