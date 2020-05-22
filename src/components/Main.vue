<template>
  <div class="main">
    <div class="banner"></div>
    <img class="profilepic" src="../assets/profilepic.jpg" />

    <div class="profile">
      <h1 class="whiteText">Farhia M Muse</h1>
      <p class="whiteText">
        Hi and welcome to my page! 🎉 My name is Farhia Muse and I'm a junior
        developer experienced in web development and test. <br />
        This site is heavily inspired by my twitter profile 🤩
      </p>
      <div class="details">
        <span class="whiteText location"
          ><i class="fa fa-map-marker"></i> Stockholm, Sweden</span
        >
        <span class="whiteText linkedin"
          ><a href="https://www.linkedin.com/in/farhiamuse/"
            ><i class="fa fa-linkedin"></i> LinkedIn</a
          ></span
        >
      </div>
    </div>

    <div class="menu">
      <button @click="aboutmeClicked()" class="whiteText aboutme">
        About me
      </button>
      <button @click="projectsClicked()" class="whiteText projects">
        Projects
      </button>
      <button @click="playlistClicked()" class="whiteText playlist">
        Playlist
      </button>
      <button @click="photographyClicked()" class="whiteText photography">
        Photography
      </button>
    </div>

    <div class="blue-line"></div>

    <div class="page">
      <div id="page1" class="active-demo"><Aboutme /></div>
      <div id="page2" class="inactive"><Projects /></div>
      <div id="page3" class="inactive"><Playlist /></div>
      <div id="page4" class="inactive"><Instagram /></div>
    </div>
  </div>
</template>

<script>
import Aboutme from "@/components/Aboutme.vue";
import Projects from "@/components/Projects.vue";
import Playlist from "@/components/Playlist.vue";
import Instagram from "@/components/Instagram.vue";

export default {
  name: "Main",
  components: {
    Playlist,
    Aboutme,
    Projects,
    Instagram
  },
  methods: {
    aboutmeClicked() {
      event.preventDefault();
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      var photography = document.getElementById("page4");

      aboutme.className = aboutme.className.replace("inactive", "active-demo");
      projects.className = projects.className.replace(
        "active-demo",
        "inactive"
      );
      playlist.className = playlist.className.replace(
        "active-demo",
        "inactive"
      );
      photography.className = photography.className.replace(
        "active-demo",
        "inactive"
      );
    },
    projectsClicked() {
      event.preventDefault();
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      var photography = document.getElementById("page4");

      aboutme.className = aboutme.className.replace("active-demo", "inactive");
      projects.className = projects.className.replace(
        "inactive",
        "active-demo"
      );
      playlist.className = playlist.className.replace(
        "active-demo",
        "inactive"
      );
      photography.className = photography.className.replace(
        "active-demo",
        "inactive"
      );
    },
    playlistClicked() {
      event.preventDefault();
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      var photography = document.getElementById("page4");

      aboutme.className = aboutme.className.replace("active-demo", "inactive");
      projects.className = projects.className.replace(
        "active-demo",
        "inactive"
      );
      playlist.className = playlist.className.replace(
        "inactive",
        "active-demo"
      );
      photography.className = photography.className.replace(
        "active-demo",
        "inactive"
      );
    },
    photographyClicked() {
      event.preventDefault();
      var aboutme = document.getElementById("page1");
      var projects = document.getElementById("page2");
      var playlist = document.getElementById("page3");
      var photography = document.getElementById("page4");

      aboutme.className = aboutme.className.replace("active-demo", "inactive");
      projects.className = projects.className.replace(
        "active-demo",
        "inactive"
      );
      playlist.className = playlist.className.replace(
        "active-demo",
        "inactive"
      );
      photography.className = photography.className.replace(
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

  .details {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    color: #738390;
    margin-top: 1.25em;

    .linkedin {
      margin-left: 2rem;
      color: #5aa8e9;
    }

    .location {
      color: #5aa8e9;
    }
  }
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
    font-size: 0.9em;
    color: #72889c;
  }

  .aboutme:hover,
  .aboutme:target {
    color: #2581cb;
  }

  .projects:hover,
  .projects:target {
    color: #2581cb;
  }

  .playlist:hover,
  .playlist:target {
    color: #2581cb;
  }

  .photography:hover,
  .photography:target {
    color: #2581cb;
  }
}

.page {
  display: flex;
  justify-content: center;
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

a {
  color: inherit;
  text-decoration: inherit;
}

h1,
p,
span,
button {
  font-family: sans-serif;
  font-weight: 400;
  line-height: 1.6;
}

.instagram-embed {
  max-width: 350px;
}


@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
  .main {
    button {
      font-size: 1.5rem;
      background: inherit;
      border: none;
    }
  }
}

@media (min-width: 1024px) {
  // desktop
  .main {
    max-width: 66.25rem;
    margin-right: auto;
    margin-left: auto;

    button {
      font-size: 1.3rem;
      background: inherit;
      border: none;
    }

    button:hover,
    button:active,
    button:focus,
    :target {
      outline: 0;
      color: #2581cb;
    }

    .page{
      .page4{
      width:900px;
      border: 1px solid red;
    }
    }
  }
}
</style>
