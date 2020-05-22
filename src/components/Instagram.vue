<template>
  <div class="instagram">
     <instagram-embed class="instagram-embed"
          :url="'https://www.instagram.com/p/B2gRThbAG7X/?utm_source=ig_web_copy_link'"
          :max-width=350
          :hide-caption=true
        />
        <instagram-embed class="instagram-embed"
          :url="'https://www.instagram.com/p/B2R3TqEA7yM/?utm_source=ig_web_copy_link'"
          :max-width=350
          :hide-caption=true
        />
        <instagram-embed class="instagram-embed"
          :url="'https://www.instagram.com/p/BogueQRnRbV/?utm_source=ig_web_copy_link'"
          :max-width=350
          :hide-caption=true
        />
         <instagram-embed class="instagram-embed"
          :url="'https://www.instagram.com/p/BbuD1dygcPQ/?utm_source=ig_web_copy_link'"
          :max-width=350
          :hide-caption=true
        />
  </div>
</template>

<script>
import InstagramEmbed from "vue-instagram-embed";

export default {
  name: "Instagram",
  components: {
    InstagramEmbed
  }
}
</script>

<style lang="scss" scoped>
.instagram{
  display:flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 2em;

  .instagram-embed{
    margin: 1rem;
  }
}


@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
  .instagram {
  
  }
}

@media (min-width: 1024px) {
  // desktop
  .instagram {
    width: 900px;
  }
}

</style>