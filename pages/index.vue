<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        mock API
      </h1>
    </div>
    <div>
       {{ data }}
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData ({ $axios, params }) {
    const data = await $axios.$get(`/users/0`)
    return { data }
  }
}
</script>
