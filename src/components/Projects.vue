<template>
  <div class="projetcs">
    <a href="https://farhiam.github.io/cupcake/">
      <img class="cupcake"
        src="../assets/cupcake.png"
        alt="Cupcake image website with link"
      />
    </a>
    <p class="description"> project description</p>
  </div>
</template>

<script>
export default {
  name: "Playlist"
};
</script>

<style lang="scss" scoped>
.projetcs{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top:2rem;

  .cucpcake{
   
  }
  img{
    height: 15rem;
    width: 20rem;
    }

  .description{
    color:white;
  }
}
</style>
