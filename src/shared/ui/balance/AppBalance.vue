<script lang="ts">
export default {}
</script>

<template>
  <div class="balance-container">
    <div class="used">
      <span class="title">Used: </span>
      <span>0.4 GB</span>
    </div>
    <div class="line"></div>
    <div class="balance">
      <span class="title">Balance: </span>
      <span>0.6 TBY</span>
    </div>

    <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path
        d="M7.5 1.5C7.5 0.671573 8.17157 0 9 0C9.82843 0 10.5 0.671573 10.5 1.5V16.5C10.5 17.3284 9.82843 18 9 18C8.17157 18 7.5 17.3284 7.5 16.5V1.5Z"
        fill="#FFD600"
      />
      <path
        d="M16.5 7.5C17.3284 7.5 18 8.17157 18 9C18 9.82843 17.3284 10.5 16.5 10.5L1.5 10.5C0.671573 10.5 -3.62117e-08 9.82843 0 9C3.62117e-08 8.17157 0.671573 7.5 1.5 7.5L16.5 7.5Z"
        fill="#FFD600"
      />
    </svg>
  </div>
</template>

<style scoped lang="scss">
.balance-container {
  padding: 10px 16px;
  display: flex;
  align-items: center;
  gap: 12px;
  justify-content: space-between;
  border: 1px solid #ebebeb;
  border-radius: 10px;

  //   .used {
  //     margin-right: 12px;
  //   }

  //   .balance {
  //     padding-left: 12px;
  //     border-left: 1px solid #ebebeb;
  //     padding-right: 12px;
  //   }
  .line {
    width: 1px;
    background-color: #ebebeb;
    height: 20px;
  }

  .title {
    font-weight: 300;
    color: #676767;
  }
}
</style>
