<template>
  <div>
    <div class="box" v-for="e in elements" v-bind:key="e.id">
      {{ e.title }}
    </div>

  </div>
</template>

<script>
//import ListDefault from "../partials/_ListDefault";
export default {
  /*components: {
    ListDefault
  },*/
  created() {
    this.findAll();
  },
  data() {
    return {
      elements: []
    };
  },
  methods: {
    findAll: function() {
      fetch("http://localhost:8000/api/element/?format=json")
        .then(res => res.json())
        .then(res => (this.elements = res));
    }
  }
};
</script>

<style >
.box {
  border: 3px solid #ccc;
  margin: 5px 0 0 0;
}
</style>