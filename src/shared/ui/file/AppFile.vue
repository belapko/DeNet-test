<script lang="ts">
export default {
  props: {
    title: { type: String, required: true },
    isActive: { type: Boolean, required: true }
  }
}
</script>

<template>
  <div class="file" :class="{ active: isActive }">
    <svg width="77" height="96" viewBox="0 0 77 96" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path
        d="M5 96H72C74.7614 96 77 93.7614 77 91V16L60 0H5C2.23858 0 0 2.23857 0 5V91C0 93.7614 2.23858 96 5 96Z"
        fill="#ACADB5"
      />
      <svg x="60">
        <path d="M5 16H17L1.90735e-06 0L0 11C0 13.7614 2.23858 16 5 16Z" fill="#FFD600" />
      </svg>
    </svg>
    <span class="title">{{ title }}</span>
  </div>
</template>

<style scoped lang="scss">
.file {
  display: inline-block;
  padding: 24px 36px 0px 37px;
  border-radius: 10px;
  cursor: pointer;

  .title {
    display: block;
    margin-top: 15px;
    padding-bottom: 19px;
    text-align: center;
    color: #232323;
  }

  &:hover:not(.active) {
    background-color: #f6f6f6;
  }

  &.active {
    background-color: #ebebeb;
  }
}
</style>
