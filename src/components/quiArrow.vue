<template>
  <button class="qui-arrow"  >
    <span >{{msg}}</span>
  </button>
</template>

<script>
  export default {
    props: {
      msg: {
        default: '冬休'
      }
    }
  }
</script>
<style scoped>
  .qui-arrow{
    width: 30px;
    height: 30px;
    background-color: yellow;
    text-align: center;
  }
  .qui-arrow span{
    line-height: 30px;
  }
</style>
