<template>
  <div>
    <p>title : {{ item.title }}</p>
    <p>time_ago : {{ item.time_ago }}</p>
    <p>content : {{ item.content }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    item () {
      return this.$store.state.item
    }
  },
  created() {
    const id = this.$route.params.id
    this.$store.dispatch('FETCH_ITEM', id)
  }
}
</script>

<style>

</style>