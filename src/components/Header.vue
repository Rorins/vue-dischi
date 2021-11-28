<template>
  <header>
     <img class="logo" src="../assets/logo.png" alt="">

<label for="disks">Select disk:</label>

<select v-model="genre" @change="$emit('search',genre)" name="disks" id="disks">
  <option value="rock">Rock</option>
  <option value="pop">Pop</option>
  <option value="jazz">Jazz</option>
  <option value="metal">Metal</option>
</select> 
  </header>
</template>

<script>
export default {
name:'Header',
data(){
  return{
    genre:'',
  }
}
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