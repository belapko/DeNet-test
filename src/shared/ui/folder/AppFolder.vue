<script lang="ts">
export default {
  props: {
    title: { type: String, required: true },
    isActive: { type: Boolean, required: true }
  }
}
</script>

<template>
  <div class="folder" :class="{ active: isActive }">
    <svg
      width="120"
      height="90"
      viewBox="0 0 120 90"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M0 84.2388V5.76716C0 2.5809 2.58297 0 5.76923 0H44.72C45.6381 0 46.5185 0.364697 47.1677 1.01386L47.7288 1.57493C48.7707 2.61688 48.7707 4.3062 47.7288 5.34815C46.0616 7.01529 47.2178 9.86707 49.5753 9.90252L114.318 10.8761C117.47 10.9235 120 13.4922 120 16.6447V84.2308C120 87.417 117.417 90 114.231 90H5.76923C2.58297 90 0 87.425 0 84.2388Z"
        fill="#FFD600"
      />
      <path
        d="M0 84.2388V9.22981C0 6.04355 2.58297 3.46154 5.76923 3.46154H12.6103C14.1404 3.46154 15.6078 4.06937 16.6898 5.15131L24.8487 13.3102C25.9306 14.3922 27.3981 15 28.9282 15H43.2692C45.1853 15 46.1449 12.6834 44.79 11.3285C43.9501 10.4886 43.9501 9.12681 44.79 8.2869L47.9256 5.15131C49.0076 4.06937 50.475 3.46154 52.0051 3.46154H114.231C117.417 3.46154 120 6.04451 120 9.23077V84.2308C120 87.417 117.417 90 114.231 90H5.76923C2.58297 90 0 87.425 0 84.2388Z"
        fill="#ACADB5"
      />
    </svg>
    <span class="title">{{ title }}</span>
  </div>
</template>

<style scoped lang="scss">
.folder {
  display: inline-block;
  padding: 24px 15px 0px;
  border-radius: 10px;
  cursor: pointer;

  .title {
    display: block;
    margin-top: 15px;
    padding-bottom: 25px;
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
