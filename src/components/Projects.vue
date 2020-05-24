<template>
  <div class="projetcs">
    <Project
      v-for= "e in elements" :key="e.description"
      :srcLink="e.srcLink"
      :srcImage="e.srcImage"
      :altText="e.altText"
      :description="e.description"
    />
  </div>
</template>

<script>
import Project from "@/components/Project.vue";

export default {
  name: "Playlist",
  components: {
    Project
  },
  data() {
    return {
      elements: [
        {
          srcLink: "https://farhiam.github.io/cupcake/",
          srcImage: "cupcake",
          altText: "alttext placeholder",
          description: "A dummy cupcake website build with Vue.js and vuex. Built together with a friend."
        },
        {
          srcImage: "placeholder",
          description: "More coming soon.."
        },
        {
          srcImage: "placeholder",
          description: "More coming soon.. "
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped></style>
