<template>
  <div id="card" class="card">
    <div v-for="result in results" :key="result.id" class="card-body">
      <h5 class="card-title">{{ result.title }}</h5>
      <h6 class="card-subtitle mb-2 text-muted">{{ result.datePosted }}</h6>
    </div>
  </div>
</template>

<script>
const Vue = require('vue')
const axios = require('axios')
const cheerio = require('cheerio')
const URL = 'https://corelight.blog/'

export default {
  data() {
    return {
      results: []
    }
  },
  created: function() {
    this.loadBlogs()
  },
  methods: {
    loadBlogs: function() {
      axios
        .get(URL)
        .then(({ data }) => {
          const $ = cheerio.load(data)
          $('.post').each((i, element) => {
            const title = $(element)
              .children('.content-inner')
              .children('.post-header')
              .children('.post-title')
              .children('a')
              .text()
            const datePosted = $(element)
              .children('.content-inner')
              .children('.post-header')
              .children('.post-meta')
              .children('.posted-on')
              .children('a')
              .children('.published')
              .text()
            this.$set(
              this.results,
              i,
              Object.assign({}, this.results, {
                id: i + 1,
                title: title,
                datePosted: datePosted
              })
            )
          })
          // console.log(this.results)
        })
        .catch(console.error)
    }
  }
}
</script>

<style>
</style>
