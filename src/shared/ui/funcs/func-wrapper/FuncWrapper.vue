<script lang="ts">
export default {
  props: {
    title: { type: String, required: true },
    isMenuItem: { type: Boolean },
    isClear: { type: Boolean }
  }
}
</script>

<template>
  <button class="button" :class="{ ['not-menu-item']: !isMenuItem, clear: isClear }">
    <div class="btn-items">
      <slot class="icon"></slot>
      <span class="title">{{ title }}</span>
    </div>
  </button>
</template>

<style scoped lang="scss">
.clear {
  box-shadow: none !important;
  border: none !important;
}

.not-menu-item {
  border-radius: 10px;
  box-shadow: 1px 5px 23px 0px #23232314;
}

.button {
  height: 44px;
  padding: 10px 12px;
  border-bottom: 1px solid #ebebeb;
  background-color: #ffffff;

  &:hover {
    background-color: #f6f6f6;
  }

  .btn-items {
    display: flex;
    align-items: center;
    gap: 6px;

    .icon {
      margin-left: 12px;
    }

    .title {
      color: #676767;
    }
  }
}
</style>
