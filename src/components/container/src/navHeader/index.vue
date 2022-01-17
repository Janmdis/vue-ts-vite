<template>
<header>
  <span @click="toggle">
    <el-icon-expand v-if="collapse"></el-icon-expand>
    <el-icon-fold v-else></el-icon-fold>
  </span>
</header>
</template>
<script lang='ts' setup>
let props = defineProps<{
  collapse: boolean
}>()
let emits = defineEmits(['update:collapse'])
let toggle = () =>{
  console.log(1111)
  emits('update:collapse', !props.collapse)
}

</script>
<style lang="scss" scoped>
header {
  height: 60px;
  padding: 0 20px;
  display: flex;
  align-items: center;
  cursor: pointer;
}
</style>