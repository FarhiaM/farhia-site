<template>
  <div class="main">
    <div class="banner"></div>
    <img class= "profilepic" src="../assets/profilepic.jpg">
    
    <div class="profile">
      <h1>Farhia Muse</h1>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantiu
        doloremque laudantium, totam rem aperiam, eaque ipsa</p>
        <div class="details">
          <span><i class="fa fa-map-marker"></i> Stockholm, Sweden</span>
          <span><i class="fa fa-linkedin"></i> LinkedIn</span>
          <span><i class="fa fa-twitter"></i> Twitter</span>
        </div>
    </div>
     <div class="menu">
        <a class="aboutme">About me</a>
        <a class="projects">Projects</a>
        <a class="playlist">Music playlist</a>
    </div>
    <div class="blue-line"></div>

  <div class="page">
    <div id="page1" class="active-demo"><Aboutme/></div>
    <div id="page2" class="inactive"><Projects/></div>
    <div id="page3" class="inactive"><Playlist/></div>
  </div>

  </div>
</template>

<script>
import Aboutme from '@/components/Aboutme.vue'
import Projects from '@/components/Projects.vue'
import Playlist from '@/components/Playlist.vue'

export default {
  name: 'Main',
  components: {
    Playlist,
    Aboutme,
    Projects
    }
};
</script>

<style lang="scss" scoped>

.banner{
  width: 100%;
  height: 150px;
  background-color: #DC5167;
}

.profilepic{
  max-width: 100px;
  max-height: 100px;
  margin-top: -30px;
  margin-left:30px;
  border-radius: 50%;
}

.profile{
  margin: 20px;
}

.details{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  color: #738390;
  margin-top: 20px;
}

p, h1{
  color: #FFFFFF;
}

.menu{
  color: white;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  list-style: none;
  margin:0;
  padding:20px;
  outline:none;
  cursor:pointer;

  .aboutme:hover, .aboutme:target{
    color: #2581CB;
  }
  
  .projects:hover{
    color: #2581CB;
  }

  .playlist:hover{
    color: #2581CB;
  }

}

  .blue-line{
    border: 1px solid #2B343C;
  }

  .active-demo {
 display:block;
}

.inactive {
  display:none;
}
@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
 
}

@media (min-width: 1024px) {
  // desktop
}

@media screen and (prefers-color-scheme: light) {
  p {
    color:black;
  }
}
</style>