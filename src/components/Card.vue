<template>
  <div class="card">
    <img :src="image" :alt="title" />
    <h3>{{title}}</h3>
    <h4>{{subTitle}}</h4>
    <h5>{{subText}}</h5>
    <h6>{{text}}</h6>      
  </div>
</template>

<script>
export default {
name: 'Card',
props:{
    image: String,
    title: String,
    subTitle: String,
    subText: String,
    text: String,
},
};
</script>

<style scoped lang='scss'>

</style>