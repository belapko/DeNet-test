<script lang="ts">
import {
  AppLogo,
  FuncUpload,
  FuncNewFolder,
  FuncRecycleBin,
  SearchButton,
  NetworkDropdown,
  AppBalance,
  AppProfile
} from '@/shared/ui'

export default {
  components: {
    AppLogo,
    FuncUpload,
    FuncNewFolder,
    FuncRecycleBin,
    SearchButton,
    NetworkDropdown,
    AppBalance,
    AppProfile
  }
}
</script>

<template>
  <header class="header">
    <div class="left-menu">
      <app-logo />
      <div class="left-submenu">
        <func-upload colorized />
        <func-new-folder />
        <func-recycle-bin :is-clear="true" />
      </div>
    </div>
    <div class="right-menu">
      <search-button />
      <network-dropdown />
      <app-balance />
      <app-profile />
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  margin: 0px 64px;
  padding: 32px 0px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .left-menu {
    align-items: center;
    display: flex;
    gap: 28px;

    .left-submenu {
      align-items: center;
      display: flex;
      gap: 20px;
    }
  }

  .right-menu {
    align-items: center;
    display: flex;
    gap: 18px;
  }
}
</style>
