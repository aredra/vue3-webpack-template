<template>
  <h2 @click="changeMessage">
    {{ msg }}
  </h2>
</template>

<script>
export default {
  computed: {
    msg() {
      return this.$store.state.message.msg
    }
  },
  methods: {
    changeMessage() {
      this.$store.dispatch('message/changeMessage', 'Hello Vue!!!')
    }
  }
}
</script>

<style scoped lang="scss">
  @import "~/scss/main";

  h2 {
    font-size: 22px;
    color: $color--primary;
    & + img {
      width: 120px;
    }
  }
</style>
