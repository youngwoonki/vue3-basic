<template>
  <li>{{ name }}?!</li>
</template>

<script>
export default{
  props:{
    name:{
      type:String,
      default:''
    }
  } // 기초값설정해준거
}
</script>

<style scoped lang="scss"> // 해당 component에만 영향을 미침
h1{
  color: red !important;
}
</style>