<template>
  <div>
    <button v-on:click="findAll">Click</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
  methods: {
    findAll: function() {
      fetch("http://localhost:8000/api/element/?format=json")
        .then(res => res.json())
        .then(res => (console.log(res)));
    }
  }
};
</script>