<template>
  <div id="app">
    <!--Header-->
    <Header @search="searchMatch" />
    <!--Main-->
    <Disks :diskList="filteredGenre" />
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
        genre:'',
    };
},
computed:{
  filteredGenre(){
    if (this.genre === ''){
      return this.disks;
    }
    //itero il mio array disks con un filter
    return this.disks.filter(item =>{
      return item.genre.toLowerCase().includes(this.genre.toLowerCase())
    });
  }
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
    searchMatch(choice){
    console.log(choice);
    this.genre = choice;
}
},
};
</script>

<style lang="scss">
@import '@/styles/globals';
</style>
