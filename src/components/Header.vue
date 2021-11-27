<template>
  <header>
     <img class="logo" src="../assets/logo.png" alt="">

<label for="disks">Select disk:</label>

<select name="disks" id="disks">
  <option value="">Rock</option>
  <option value="">Pop</option>
  <option value="">Jazz</option>
  <option value="">Metal</option>
</select> 
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