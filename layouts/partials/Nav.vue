<template>
  <header>
    <b-nav class="container">
      <b-nav-item>
        <nuxt-link 
          to="/" 
          class="text-white">Home
        </nuxt-link>
      </b-nav-item>
      <b-nav-item>
        <nuxt-link 
          to="/" 
          class="text-white">Bulletins
        </nuxt-link>
      </b-nav-item>
      <b-nav-item>
        <nuxt-link 
          to="/" 
          class="text-white">About
        </nuxt-link>
      </b-nav-item>
      <b-nav-item>
        <nuxt-link 
          to="/" 
          class="text-white">Contact
        </nuxt-link>
      </b-nav-item>
      <b-nav-item><a
        class="text-white"
        href="https://corelight.com/" 
        target="_blank">Corelight.com</a></b-nav-item>
    </b-nav>
  </header>
</template>

<script>
export default {}
</script>

<style scoped>
header {
  background-color: #2e3438;
}

.text-white {
  color: #ffffff;
}

.nav-item {
  margin: 10px;
}
</style>
