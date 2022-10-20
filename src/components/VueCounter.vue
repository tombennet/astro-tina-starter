<template>
  <h2>{{ variableExample }}</h2>
  <div>Count: {{ count }}</div>
  <button @click="subtract">-</button>
  <button @click="add">+</button>
</template>

<script>
export default {
  name: "VueCounter",
  props: {
    variableExample: String,
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    add() {
      this.count++;
    },
    subtract() {
      this.count--;
    },
  },
};
</script>