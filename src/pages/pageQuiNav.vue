<template>
  <div id="pageQuiNav">
    <qui-nav msg="确定" class="small" v-on:navClickEvent="dos">
    </qui-nav>
  </div>
</template>
<script>
  import quiNav from '../components/quiNav.vue'
  export default {
    name: 'pageQuiButton',
    components: {
      'qui-nav': quiNav
    }
  }
</script>
<style scoped>

</style>
