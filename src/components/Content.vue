<template>
  <div class="grid col-span-full xl:col-span-8  gap-10">
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