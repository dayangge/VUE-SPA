<template>
  <div class="qui-nav nav-type-1">
    <a v-for="(item,index) in items" :class="[commonClass,item.active ? activeClass : '']" v-on:click="navClickEvent(items,index)" >
      <span class="nav-txt">{{item.text}}</span>
    </a>
  </div>
</template>
<script>
  export default {
    data: function () {
      return {
        commonClass: 'nav-item',
        activeClass: 'active',
        items: [
          {
            text: '首页',
            active: true
          },
          {
            text: '列表',
            active: false
          },
          {
            text: '关于',
            active: false
          },
          {
            text: '招聘',
            active: false
          }
        ]
      }
    },
    methods: {
      navClickEvent: function (items, index) {
        items.forEach(function (el) {
          el.active = false
        })
        items[index].active = true
        this.$emit('navClickEvent', items, index)
      }
    }
  }
</script>
<style scoped>
.nav-item{
  width: 60px;
  height: 48px;
  font-size: 20px;
  background-color:#af4521;
  border: 1px solid seagreen;
  box-sizing: border-box;
  margin: 0 5px;
  color: aliceblue;
  float: left;
  cursor: pointer;
}
.qui-nav .active{
  border-bottom: 5px solid yellow;
}
</style>
