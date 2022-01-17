<template>
  <el-aside width="auto">
    <el-menu
    default-active="1"
    :collapse="collapse"
    class="el-menu-vertical-demo">
    <el-menu-item index="1">
      <el-icon><el-icon-menu /></el-icon>
      <span>Navigator one</span>
    </el-menu-item>
      <el-menu-item index="2">
      <el-icon><el-icon-setting /></el-icon>
      <span>Navigator Two</span>
    </el-menu-item>
      <el-menu-item index="3">
      <el-icon><el-icon-document /></el-icon>
      <span>Navigator three</span>
    </el-menu-item>
    </el-menu>
  </el-aside>
</template>
<script lang='ts' setup>
  let props = defineProps<{
    collapse: boolean
  }>()
</script>
<style lang="scss" scoped>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
}
</style>