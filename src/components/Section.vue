<template>
<div>
  <div clasS="container">
    <img class="profilepic" src="../assets/profilepic.png" />
    <div class="section-container">
      <h2 class="section-name">Farhia M Muse</h2>
      <h3 class="section-handle">@Farhia_MM</h3>
      <p class="section-text">{{text}}</p>
    </div>
  </div>
  <div class="blue-line"></div>
  </div>
</template>

<script>
export default {
  name: "Section",
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>

.container{
  display: flex;
  flex-direction: row;
  margin: 1.25rem;
  color:white;

  .section-container{
    margin-left: 1rem;

    .section-name{
      color:white;
      font-size: 1rem;
      display: inline;
    }

    .section-handle{
      color: #758491;
      font-size: 1rem;
      display: inline;
      margin-left: 0.7rem;
    }

    .section-text{
      color: white;
      font-size: 1rem; 
    }
  }
  
  .profilepic{
    height: 51px;
    width:51px;
    border-radius: 50%
    }
}

.blue-line {
  border: 0.05em solid #1f262c;;
  }

  h2,h3,p{
  font-family:sans-serif;
  font-weight: 400;
  line-height: 1.3
}
</style>