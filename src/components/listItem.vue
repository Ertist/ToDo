<template>
    <div @click = "handleDelete">{{content}}</div>
</template>

<script>
export default {
  props: ['content', 'index'],
  data () {
    return {

    }
  },
  methods: {
    handleDelete: function (index) {
      this.$emit('itemDelete', index)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
