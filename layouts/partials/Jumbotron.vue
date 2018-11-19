<template>
  <div class="jumbotron">
    <div 
      id="jumbotron"
      class="container">
      <h1 
        id="logo" 
        class="display-1 jumbotron-text">
        <b-img
          :src="require('@/assets/images/u5t8-rrk_400x400.jpg')"
          rounded="circle"
          class="mr-4"
          alt="logo"
          width="150"
          height="150"
        />
        Corelight Blog
      </h1>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.jumbotron {
  background-color: #2e3438;
  border-radius: 0px;
}
h1 {
  color: #ffffff;
}
</style>
