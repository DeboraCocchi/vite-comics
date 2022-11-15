<script>
export default {
  name:'AppHeader'
}
</script>

<template>
  <header class="d-flex">
    <div class="container">
      <div class="logo">
      <img src="/dc-logo.png" alt="DC Logo">
    </div>
    </div>
    
  </header>
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;

  header{
    background-color: white;
    height:85px;
    margin-top:30px;
    .logo{
      padding:10px;
    }
  }
</style>