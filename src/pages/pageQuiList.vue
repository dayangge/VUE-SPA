<template>
  <div id="pageQuiPage">
  <qui-list tipsText="自定义文案，默认右边是按钮" msg="弹层"></qui-list>
  <qui-list v-on:btnClickEvent="test"></qui-list>
  <qui-list ref="child1" tipsText="最右边是箭头" currentView="qui-arrow"></qui-list>
  </div>
</template>
<script type="text/ecmascript-6">
  import quiList from '../components/quiList.vue'
  export default {
    name: 'pageQuiList',
    components: {
      'qui-list': quiList
    },
    methods: {
      test: function () {
        alert('我是自定义方法')
      }
    }
  }
</script>
<style>

</style>
