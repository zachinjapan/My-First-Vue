<template>
  <div>
    <h1>ランダムキツネ</h1>
    <button @click="fetchFoxImage">Get Random Fox</button>
    <img :src="imageURL" loading="lazy" alt="Random fox" />
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

<style scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  width: 500px;
  height: 500px;
}
</style>
