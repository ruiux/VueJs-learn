<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-3 p-3">
        <div class="col-lg-12">
          <h2>Detail Tugas</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="list-tugas text-left p-2">
            <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas pb-3">

              <itemTugas v-bind:tugasSaya="tugasSaya"/>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../node_modules/bootstrap/dist/css/bootstrap.css";
import itemTugas from './components/itemTugas.vue'

export default {
  name: "App",
  data: function() {
    return {
      tugas: [
        {
          id: 1,
          namaTugas: "Ngoding",
          isDone: false
        },
        {
          id: 2,
          namaTugas: "Kerjain Live",
          isDone: false
        },
        {
          id: 3,
          namaTugas: "Makan",
          isDone: false
        },
        {
          id: 4,
          namaTugas: "Tidur",
          isDone: false
        }
      ]
    };
  },
  components: {
    itemTugas
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header {
  background-color: #1abc9c;
}
.header h2 {
  margin: 0;
}
.item-completed {
  color: #1abc9c;
}
</style>
