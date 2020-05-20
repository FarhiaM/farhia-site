<template>
  <div class="aboutme">
    <Section v-for= "t in texts" :key="t.text" :text="t.text"/>
  </div>
</template>

<script>
import Section from "@/components/Section.vue";

export default {
 name: "Aboutme",
 components: {
    Section
  },
  data () {
    return {
      texts: [
        {
          text: 'Tart marzipan tart pastry cake jelly-o. Sugar plum pudding macroon liqriouse I love. Pastry dessert cookie tart. I love I love topping danish.'
        },
        {
          text: 'Halvah wypas pudding I love candy toffee. Jelly beans chupa chups pudding danish I love donut. I love danish bonbon jelly-o I love gummies cotton candy marzipan danish. Donut sweet pastry jujubes croissant.'
        },
        {
          text: 'Liquorice toffee marzipan lemon drops chocolate cake ice crearri.'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.aboutme{
  padding: 0;
}

</style>