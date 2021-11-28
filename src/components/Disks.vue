<template>
  <section>
      <div class="container-fluid">
          <div class="row d-flex justify-content-center">
            
              <div v-for="(disk,index) in diskList" :key="`disk${index}`" class="col-2">
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
import Card from '@/components/Card.vue';

export default {
name:'Disks',
components:{
  Card,
},
props:{
    diskList:Array
}
}
</script>

<style scoped lang="scss">
section{
    background-color: #1d2d3c;
    padding:100px 0;
}
       .col-2{
           margin-bottom:20px;
       }
.card{
    background-color:#2e3a46;
    color:white;
    padding:20px;
}
   
</style>