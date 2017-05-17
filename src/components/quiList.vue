//quiList.vue

<template>
  <div class="qui-list">
    <span class="list-tips">{{tipsText}}</span>
    <component :is="currentView" v-on:btnClickEvent="ClickEvent" :msg=msg class="small" keep-alive></component>
  </div>
</template>

<script>
  import quiButton from '../components/quiButton.vue'
  import quiArrow from '../components/quiArrow.vue'
  export default{
    props: {
      msg: {
        default: '下载'
      },
      tipsText: {
        default: '默认的文案'
      },
      currentView: {
        default: 'qui-btn'
      },
      btnClickEvent: {
        type: Function,
        default: function () {
          alert(this.msg + '我是默认事件')
        }
      }
    },
    components: {
      'qui-btn': quiButton,
      'qui-arrow': quiArrow
    },
    methods: {
      ClickEvent: function () {
        this.btnClickEvent()
        this.$emit('btnClickEvent')
      }
    }
  }
</script>
