<script>
export default {
  name:'AppMain'
}
</script>

<template>
  <div class="container">
    <h2>--> Content Goes Here &lt;-- </h2>
  </div>
</template>


<style lang="scss" scoped>
  @use '../style/partials/variables' as *;
  @use '../style/partials/mixin' as *;

  .container{
    padding:30px 0;
    height:130px;
    h2{
      font-size:2.2rem;
    }
  }
</style>