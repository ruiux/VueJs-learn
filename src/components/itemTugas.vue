<template>
  <div class="form-check">
    <input class="form-check-input" onclick type="checkbox" value id="defaultCheck1" />
    <label
      class="form-check-label"
      v-bind:class="{'item-completed':tugasSaya.isDone}"
      for="defaultCheck1"
    >{{tugasSaya.namaTugas}}</label>
  </div>
</template>


<script>
export default {
    name: "itemTugas",
    props:[
        "tugasSaya"
    ]
};
</script>

<style scoped>
</style>