<template>
  <div class="contactContainer">
    <div class="spotifyWidget">
      <iframe
        src="https://open.spotify.com/embed/playlist/6WhyfvYNU4M1Kdy1LHpVpR"
        width="300"
        height="380"
        frameborder="0"
        allowtransparency="true"
        allow="encrypted-media"
      ></iframe>
    </div>
  </div>
</template>

<script>
export default {
   name: "Playlist"
};
</script>

<style lang="scss" scoped>
.contactContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin:20px;
}


.spotifyWidget {
  flex: 50%;
  margin-bottom: 40px;
}

@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
}

@media (min-width: 1024px) {
  .spotifyWidget {
    flex: 50%;
  }
}
</style>
