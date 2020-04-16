<template>
  <header>
    <!-- 6. props data 사용 -->
    <h1>{{ propsdata }}</h1>
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
  export default {
    // 5. props data 받기
    props: ['propsdata'],
    methods: {
      sendEvent: function() {
        this.$emit('renew')
      }
    }
  }
</script>

<style>

</style>