<template>
  <div class="about">
    <div class="container">

      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h3 >What I do Today</h3>
        </div>
      </div>

        <div class="row content">
          <div class="col-lg-12">
            <div class="pekerjaan-rumah">
              <div class="row">
                <div
                  v-for="tugasSaya in tugas"
                  v-bind:key="tugasSaya.id"
                  class="tugas col-lg-12 mb-3 text-left">
                <itemTugas
                  v-bind:tugasSaya="tugasSaya" />
                </div>
              </div>
            </div>
          </div>
        </div>

    </div>
  </div>
</template>

<script>
import itemTugas from "../components/itemTugas";

  export default {
    name:'About',
    components:{
      itemTugas
    },
    data : function(){
      return{
        tugas:[
          {
            id:1,
            nama :'membersihkan kamar',
            isDone :false
          },
          {
            id:2,
            nama :'Jalan-jalan',
            isDone :false
          },
          {
            id:3,
            nama :'Nonton',
            isDone :false
          }
        ]
      }
    },
  }

</script>

<style>
  .header{
    background: #1adc9c;
  }

  .header h3{
    margin: 0;
  }

  .tugas .item{
    font-size: 20px;
    /* text-align: left; */
  }

  .item-completed{
    color: #1adc9c;
  }

</style>