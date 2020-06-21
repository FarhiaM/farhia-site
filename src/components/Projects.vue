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
          altText: "Screenshot of the cupcake website",
          description: "A dummy cupcake website build with Vue.js and vuex. Built together with a friend."
        },
        {
          srcLink: "https://farhiam.github.io/rockpaperscissors/",
          srcImage: "rockpaperscissors",
          altText: "Screenshot of the game rock papper scissors",
          description: "A simple rock papper scissors game built with Vue.js and vuex. Also includes error handling when user doesn't pick one of the choices."
        },
        {
          srcLink: "https://farhiam.github.io/talo/",
          srcImage: "talo",
          altText: "Screenshot of an advice generator website",
          description: "Talo is an advice generator built using the Advice Slip JSON API."
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped></style>
