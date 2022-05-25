<template>
  <div>
    <h1>Counter</h1>
    <p>
      <button @click="increment">+</button>
      <span> {{ counter }} </span>
      <button @click="decrement">-</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "MyCounter",
  data() {
    return {
      counter: 0,
    };
  },

  methods: {
    increment() {
      this.counter++;
    },

    created() {
      console.log("MyCounter created");
    },

    decrement() {
      this.counter--;
    },
  },
};
</script>

<style scoped>
h1 {
  color: green;
}
</style>
