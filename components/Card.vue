<template>
  <div class="box-row">
    <div class="box-col" v-for="(item, key) in cards" :key="key">
      <div class="img">
        <img :src="item.previewPictureSrc" alt="" />
      </div>
      <div class="title">
        {{ item.title }}
      </div>
      <div class="text">
        {{ item.previewContext }}
      </div>
      <button>立即前往></button>
    </div>
  </div>
</template>


<script>
export default {
  props: ["cards"],
  created() {
    console.log(this.cards);
  },
};
</script>

<style scoped >
.box-row {
  box-sizing: border-box;
  margin: 20px auto;
  width: 1029px;
  height: 388px;
  display: flex;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  overflow: hidden;

  /* background-color: aqua; */
}
.box-row .box-col {
  margin-right: 30px;
  width: 323px;
  height: 100%;
}
.box-row .box-col:nth-child(3) {
  margin-right: 0;
}
.box-row .img {
  width: 100%;
  height: 170px;
}
img {
  width: 100%;
  height: 100%;
}
button {
  background-color: gray;
  color: #fff;
  padding: 10px;
  margin: 18px auto;
  width: 108px;
  height: 40px;
  font-size: 14px;
  display: block;
}
.box-row .title {
  box-sizing: border-box;
  width: 100%;
  font-size: 20px;
  text-align: center;
  padding: 15px;
}
.box-row .text {
  box-sizing: border-box;
  width: 100%;
  padding: 0 15px;
  font-size: 16px;
  height: 100px;
  overflow: hidden;
}
</style>