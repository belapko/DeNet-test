<script lang="ts">
export default {}
</script>

<template>
  <div class="container">
    <h6 class="title">All files</h6>
    <button class="dropdown">
      <span>Sort by name</span>
      <svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M10.9393 14.8533C11.5251 15.4392 12.4749 15.4392 13.0607 14.8533L18.3536 9.56008C18.5488 9.36481 18.5488 9.04823 18.3535 8.85297C18.1583 8.65772 17.8417 8.65773 17.6464 8.853L12.3536 14.1463C12.1583 14.3415 11.8417 14.3415 11.6464 14.1463L6.35357 8.853C6.15831 8.65773 5.84173 8.65772 5.64646 8.85297C5.45119 9.04823 5.45118 9.36481 5.64643 9.56008L10.9393 14.8533Z"
          fill="#232323"
        />
      </svg>
    </button>
  </div>
</template>

<style scoped lang="scss">
.container {
  margin: 0px 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .title {
    padding: 4px 10px;
    color: #676767;
    border-radius: 10px;

    &:hover {
      background-color: #f6f6f666;
    }
  }

  .dropdown {
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 9px;
    border: 1px solid #ebebeb;
    border-radius: 10px;

    &:hover {
        background-color: #F6F6F666;
    }
  }
}
</style>
