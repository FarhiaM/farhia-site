<template>
  <div class="aboutme">
    <Section class="section" v-for= "t in texts" :key="t.text" :text="t.text"/>
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
          text: 'Currently, I work for a Swedish Government Agency where I have used my skills of frontend and backend development as well as automated testing to build public and responsive web applications.'
        },
        {
          text: 'I have experience in Java, HTML/CSS, javascript, handlebarsJS, selenium, TestNG, Spring, JUnit, Jenkins/GO and Vue. I love challenging myself and consistently learning something new.'
        },
        {
          text: 'I am also passionate about diversity and digital democracy. I am active in organizations such as Kodcentrum where I spend time volunteering and teaching kids how to code.'
        },
        {
          text: 'In 2019, I was Nominated and shortlisted for the 2019 Bonnier’s Rising Star in Tech award, and it’s given me an even bigger drive and passion for the causes that are important to me. Teaching and inspiring kids to reach their full potential by coding is a privilege and an honor that I don’t take for granted.'
        },
        {
          text: 'I have also participated in hackathons such as Hack for Sweden where my team was chosen as one of the top 10 in 2018 out of 60+ teams. I also won bronze medal in the 2019 Hack for Sweden. 🥉'
        },
        {
          text: 'In my spare time, I love listening to music and taking pictures. Check out the playlist tab to listen to my favorite music right now on Spotify! 🎧! Also, take a look at the photography tab to see some of my favorite shots on Instagram! 📸 '
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

.section:hover { 
background-color: #192734 !important;
-webkit-transition: background-color 20ms linear;
-ms-transition: background-color 200ms linear;
transition: background-color 200ms linear;
padding-top: 5px;
}

</style>