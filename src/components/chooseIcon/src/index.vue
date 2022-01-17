<template>
  <el-button @click="handleClick" type="primary">
      <slot></slot>
  </el-button>
  <el-dialog :title="title" v-model="dialogVisible">11111</el-dialog>
</template>
<script lang='ts' setup>
import { watch, ref } from "vue"
let props = defineProps<
  {
    title: string,
    visible: boolean
  }
>()
let emits = defineEmits(['update:visible'])
let dialogVisible = ref<boolean>(props.visible)
let handleClick = () =>{
  emits('update:visible',!props.visible)
}
watch(()=>props.visible,val=>{
  dialogVisible.value = val
})
watch(()=>dialogVisible.value,val=>{
  emits('update:visible',val)
})
</script>
