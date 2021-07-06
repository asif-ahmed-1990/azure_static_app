<template>
  <div>
    <div>Hello {{ value }}</div>
    <button @click="fetchdata">Make Function Call</button>
    {{jsondata}}
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      value: "World",
      jsondata: '',
    };
  },
  methods: {
    async fetchdata() {
      const data = await fetch('/api/Sum');
      this.jsondata = data;
    }
  },
};
</script>
