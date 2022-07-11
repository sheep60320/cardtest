<template>
  <div class="container">
    <div>
      <Card :cards="cards" />
    </div>
  </div>
</template>

<script>
import Card from "~/components/Card.vue";
import axios from "axios";

export default {
  components: {
    Card,
  },
  data() {
    return {
      cards: [],
      apiUrl: "https://event.smarter.com.tw/api/spa/bestseller/interview",
    };
  },
  created() {
    axios
      .get(this.apiUrl)
      .then((response) => {
        //console.log(response);
        this.cards = response["data"]["data"];
        console.log(this.cards);
      })
      .catch((error) => console.log(error));
  },
};
</script>

<style scoped >
.container {
  box-sizing: border-box;
  max-width: 1029px;
}
</style>