<template>
  <section>
      <div class="container">
          <div class="row">
            
              <div v-for="(disk,index) in disks" :key="`disk${index}`" class="col-2">
                  <Card 
                  :image="disk.poster"
                  :title="disk.title"
                  :subTitle="disk.author"
                  :subText="disk.year"
                  :text="disk.genre"
                  />
                  </div>
              
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import Card from '@/components/Card.vue';

export default {
name:'Disks',
components:{
  Card,
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
    }
}
}
</script>

<style scoped lang="scss">
section{
    background-color: #1d2d3c;
}
       .col-2{
           margin:20px;
       }
.card{
    background-color:#2e3a46;
    color:white;
    padding:20px;
}
   
</style>