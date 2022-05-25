<template>
  <div>
    <h1>Random Fox</h1>
    <img :src="imageURL" alt="Random fox" />
    <button @click="fetchFoxImage">Get Random Fox</button>
  </div>
</template>

<script>
export default {
  name: "RandomFox",
  data() {
    return {
      imageURL: "",
    };
  },

  methods: {
    async fetchFoxImage() {
      const apiURL = "https://randomfox.ca/floof/?ref=apilist.fun";

      const response = await fetch(apiURL);

      const data = await response.json();

      this.imageURL = data.image;

      console.log(data);

      console.log(this.imageURL);

      return;
    },
  },

  created() {
    this.fetchFoxImage();
  },
};
</script>

<style scoped></style>
