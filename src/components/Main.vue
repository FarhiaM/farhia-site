<template>
  <div class="main">
    <div class="banner"></div>
    <img class="profilepic" src="../assets/profilepic.jpg" />

    <div class="profile">
      <h1 class="whiteText">Farhia Muse</h1>
      <p class="whiteText">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantiu doloremque laudantium, totam rem aperiam, eaque ipsa
      </p>
      <div class="details">
        <span class="whiteText"
          ><i class="fa fa-map-marker"></i> Stockholm, Sweden</span
        >
        <span class="whiteText"><i class="fa fa-linkedin"></i> LinkedIn</span>
        <span class="whiteText"><i class="fa fa-twitter"></i> Twitter</span>
      </div>
    </div>

    <div class="menu">
      <button @click="aboutmeClicked()" class="whiteText aboutme">About me</button>
      <button @click="projectsClicked()" class="whiteText projects">Projects</button>
      <button @click="playlistClicked()" class="whiteText playlist">Music playlist</button>
    </div>

    <div class="blue-line"></div>

    <div class="page">
      <div id="page1" class="active-demo"><Aboutme/></div>
      <div id="page2" class="inactive"><Projects /></div>
      <div id="page3" class="inactive"><Playlist /></div>
    </div>
  </div>
</template>

<script>
import Aboutme from "@/components/Aboutme.vue";
import Projects from "@/components/Projects.vue";
import Playlist from "@/components/Playlist.vue";

export default {
  name: "Main",
  components: {
    Playlist,
    Aboutme,
    Projects
  },
  methods: {
    aboutmeClicked() {
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      aboutme.className = aboutme.className.replace("inactive", "active-demo");
      projects.className = projects.className.replace(
        "active-demo",
        "inactive"
      );
      playlist.className = playlist.className.replace(
        "active-demo",
        "inactive"
      );
    },
    projectsClicked() {
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      aboutme.className = aboutme.className.replace("active-demo", "inactive");
      projects.className = projects.className.replace(
        "inactive",
        "active-demo"
      );
      playlist.className = playlist.className.replace(
        "active-demo",
        "inactive"
      );
    },
    playlistClicked() {
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      aboutme.className = aboutme.className.replace("active-demo", "inactive");
      projects.className = projects.className.replace(
        "active-demo",
        "inactive"
      );
      playlist.className = playlist.className.replace(
        "inactive",
        "active-demo"
      );
    }
  }
};
</script>

<style lang="scss" scoped>
.banner {
  width: 100%;
  height: 9.375em;
  background-color: #dc5167;
}

.profilepic {
  max-width: 6.25em;
  max-height: 6.25em;
  margin-top: -1.875em;
  margin-left: 1.875em;
  border-radius: 50%;
}

.profile {
  margin: 1.25em;
}

.details {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  color: #738390;
  margin-top: 1.25em;
}

.whiteText {
  color: #ffffff;
}

.menu {
  color: white;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  list-style: none;
  margin: 0;
  padding: 1.25em;
  outline: none;
  cursor: pointer;

  button {
    font-size: 1em;
  }

  .aboutme:hover,
  .aboutme:target {
    color: #2581cb;
  }

  .projects:hover {
    color: #2581cb;
  }

  .playlist:hover {
    color: #2581cb;
  }
}

.blue-line {
  border: 0.063em solid #2b343c;
}

.active-demo {
  display: block;
}

.inactive {
  display: none;
}
@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
}

@media (min-width: 1024px) {
  // desktop
}

@media screen and (prefers-color-scheme: light) {
  p {
    color: black;
  }
}
</style>
