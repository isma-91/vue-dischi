<template>
  <div class=" header d-flex align-items-center p-5">
    <div class="logo">
      <img src="@/img/logo-small.svg" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderPage',
};
</script>

<style lang="scss" scoped>
.header {
  height: 5vh;
  background-color: #2E3A46;
    img {
      width: 50px;
    }
}
</style>
