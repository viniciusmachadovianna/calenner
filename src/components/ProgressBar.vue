<template>
<div>
  <div class="hour" :style="{height:`${ hour*10}px`}"></div>
</div>
</template>
<script setup>
  import dayjs from 'dayjs'
  const hour = dayjs().hour()
</script>
<style scoped>
div{
  width:10px;
  height:240px;
  background-color: #eee;
  position: absolute;
}
.hour{
  background-color: blue;
  width: 10px;
}

</style>