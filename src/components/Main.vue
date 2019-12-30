<template>
  <div class="main">
   <div class="infoText">
     <p>Hi, I'm Farhia</p>
     <p>I'm a developer from Stockholm, Sweden</p>
   </div>
   <div class="profile">
     <p>profile pic</p>
   </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>

.main{
  display: flex;
  flex-direction: column;
  height:100vh;
  background:rgb(255, 0, 0);
  color:#fff;
}

.infoText{
  flex: 50%;
}

.profile{
  flex: 50%;
}

@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
 
}

@media (min-width: 1024px) {
  // desktop
  
 .main{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  height:100vh;
  background:rgb(255, 0, 0);
  color:#fff;
}

.infoText{
  flex: 50%;
}

.profile{
  flex: 50%;
}
}
</style>