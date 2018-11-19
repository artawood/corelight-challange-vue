<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{ blogTitle }}</h5>
      <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
      <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
      <a 
        href="#" 
        class="card-link">Like</a>
      <a 
        href="#" 
        class="card-link">Comment</a>
    </div>
  </div>
</template>

<script>
const Vue = require('vue')
const axios = require('axios')
const cheerio = require('cheerio')
const URL = 'https://corelight.blog/'

const vm = new Vue({
  el: '#app',
  data: {
    blogTitle: 'Hello!',
    datePosted: '',
    author: '',
    summary: '',
    details: '',
    imageURL: ''
  }
})

vm.blogTitle = 'This is the blog title'
</script>

<style>
</style>
