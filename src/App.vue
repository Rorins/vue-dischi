<template>
  <div id="app">
    <!--Header-->
    <Header @search="searchMatch" />
    <!--Main-->
    <Disks :diskList="disks" />
  </div>
</template>

<script>
import axios from 'axios';
import Header from '@/components/Header.vue';
import Disks from '@/components/Disks.vue';


export default {
  name: "App",
  components: {
    Header,
    Disks,
  },
  data(){
    return{
        disks:[],
    };
},
created(){
this.getDisks();
},
methods:{
    getDisks(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(result =>{
        this.disks = result.data.response;
    })
    },
    searchMatch(){
    console.log("ciao");
}
},
};
</script>

<style lang="scss">
@import '@/styles/globals';
</style>
