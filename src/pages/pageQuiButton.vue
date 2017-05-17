<template>
  <div id="pageQuiButton">
    <qui-btn msg="确定" class="small" v-on:btnClickEvent="dos1">
      <img slot="icon" class="ico" src="./img/decrease_2@2x.png">
    </qui-btn>
    <qui-btn msg="大方" class="small" v-on:btnClickEvent="dos1"></qui-btn>
  </div>
</template>
<script>
  import quiBtn from '../components/quiButton.vue'
  export default {
    name: 'pageQuiButton',
    components: {
      'qui-btn': quiBtn
    },
    methods: {
      dos1: function () {
        console.log('你点击了组件  ')
      }
    }
  }
</script>
<style scoped>

</style>
