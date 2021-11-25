<template>
  <header>
     <img class="logo" src="../assets/logo.png" alt="">
  </header>
</template>

<script>
export default {
name:'Header',
}
</script>

<style scoped lang="scss">
header{
    height: 70px;
    background-color: #2e3a46;
    display:flex;
    align-items: center;
}
.logo{
  width: 50px
}
</style>