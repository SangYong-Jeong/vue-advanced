<template>
  <div>
    ask
  </div>
</template>

<script>
import { fetchAskList } from '../api/index.js'

export default {
  created() {
    fetchAskList()
      .then(function(response) {
        console.log(response)
      })
      .catch(function(error) {
        console.log(error)
      })
  }
}
</script>

<style>

</style>