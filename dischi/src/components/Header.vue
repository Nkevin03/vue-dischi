<template>
  <header>
      <img src="@/assets/logo.png" alt="logo">
  </header>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
    @import '@/styles/variables.scss';
    header{
        background-color: $secondary-color;
        padding: 10px;

        img{
            width: 80px;
        }
    }
</style>