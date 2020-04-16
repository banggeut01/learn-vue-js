<template>
  <div>
    {{ str }}
    <!-- 4. v-bind -->
    <!-- <app-header :(하위 컴포넌트의)프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
    <app-header 
    :propsdata="str"
    v-on:renew="renewStr"
    ></app-header>
  </div>
</template>

<script>
// 1. 컴포넌트 가져오기
import AppHeader from './components/AppHeader.vue'
// var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }
export default {
  data: function() {
    return {
      // 3. data 내리기
      str: 'Header'
    }
  },
  // 2. 컴포넌트 연결
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'hi'
    }
  }
}
</script>

<style>

</style>