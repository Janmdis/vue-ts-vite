<template>
<div>
  {{visible}}
  <m-choose-icon v-model:visible="visible" title="选择图标">
    选择图标
  </m-choose-icon>
</div>
</template>

<script lang='ts' setup>
import mChooseIcon from '../../components/chooseIcon/src/index.vue'
import {ref} from 'vue'
let visible = ref<boolean>(false)
</script>

<style>

</style>