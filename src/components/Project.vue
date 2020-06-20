<template>
  <div class="project">
    <a v-bind:href="srcLink">
      <img 
      v-bind:src="require(`../assets/${srcImage}.png`)"
      v-bind:alt="altText"
      />
    </a>
    <p class="description">{{description}}</p>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: {
    srcLink: {
      type: String,
      required: false
    },
    srcImage: {
      type: String,
      required: true
    },
    altText: {
      type: String,
      required: false
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.project{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top:2rem;

  img{
    height: 15rem;
    width: 20rem;
    }
    
    p{
      margin-left: 3rem;
      margin-right: 3rem;
    }
  .description{
    color:white;
  }
}

p{
  font-family:sans-serif;
  font-weight: 400;
  line-height: 1.6
}

 img:hover,
  img:target{
    border: solid 3px #CCC;
  }

@media (min-width: 768px) and (max-width: 1023px) {
   // ipad
  .project {
   display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top:2rem;
  img{
    height: 30rem;
    width: 40rem;
    }
  }

}

@media (min-width: 1024px) {
  // desktop
  .project {
   display: flex;
  flex-direction: column;
  align-items: center;
  margin-top:2rem;
  width: 40rem;
  img{
    height: 30rem;
    width: 40rem;
    }
  }

}
</style>