<template>
  <div class="about">
    <h3>What I do Today</h3>
    <div class="pekerjaan-rumah">

      <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas">
        <p>{{tugasSaya.nama}}</p>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name:'About',
    data : function(){
      return{
        tugas:[
          {
            id:1,
            nama :'membersihkan kamar'
          },
          {
            id:2,
            nama :'Jalan-jalan'
          }
        ]
      }
    },
  }

</script>

<style  scoped>

</style>