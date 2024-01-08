<script lang="ts">
import { FuncUpload, FuncNewFolder, FuncDeleted, FuncInfo } from '@/shared/ui'
export default {
  components: { FuncUpload, FuncNewFolder, FuncDeleted, FuncInfo },
  props: {
    isActive: { type: Boolean, required: true },
    pageX: { type: Number, required: true },
    pageY: { type: Number, required: true }
  }
}
</script>

<template>
  <div v-show="isActive" class="menu" :style="{ left: pageX + 'px', top: pageY + 'px' }">
    <func-upload is-menu-item colorized />
    <func-new-folder is-menu-item />
    <func-deleted is-menu-item />
    <func-info is-menu-item />
  </div>
</template>

<style scoped lang="scss">
.menu {
  position: absolute;
  width: 150px;
  display: flex;
  flex-direction: column;
  box-shadow: 7px 9px 27px 0px #0000001f;
  border-radius: 10px;
  overflow: hidden;
  z-index: 2;
}
</style>
