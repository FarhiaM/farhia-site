<template>
  <header class="header" role="banner">
    <nav>
      <ul>
        <li><a>About</a></li>
        <li><a>Socials</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>

ul{
  list-style-type: none;
}

.header {
  display: grid;
  grid-template-rows: repeat(1, 1fr);
  grid-gap: 20;
  padding: 10px;
  align-items: center;
  justify-content: space-evenly;
}

.navContainer {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  margin: 0 auto;
}

 nav{
    grid-area: nav;
  }

@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
  .header {
   
  }
}

@media (min-width: 1024px) {
  // desktop
  .header {
    
  }
}
</style>