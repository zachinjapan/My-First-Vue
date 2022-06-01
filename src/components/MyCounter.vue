<template>
  <div>
    <h1>カウンター</h1>
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

button {
  background-color: #ccc;
  border: 1px solid #999;
  padding: 5px 10px;
  margin: 5px;
  color: green;
}

span {
  font-size: 1.5em;
}
</style>
