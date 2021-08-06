<template>
  <div class="info">
    <div
      class="info_img"
      v-if="!isRight"
      :style="{ 'background-image': 'url(' + img + ')' }"
    ></div>
    <div class="info-text">
      <h3>{{ title }}</h3>
      <p>
        {{ text }}
      </p>
    </div>
    <div
      class="info_img"
      v-if="isRight"
      :style="{ 'background-image': 'url(' + img + ')' }"
    ></div>
  </div>
</template>

<script>
export default {
  name: "InfoFlor",
  props: {
    isRight: Boolean,
    title: String,
    text: String,
    img: String
  },
};
</script>

<style lang="scss" scoped>
.info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 130px auto;
  margin-bottom: 0;
  max-width: 821px;
  width: 100%;
  &_img {

    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    width: 240px;
    height: 240px;
    border-radius: 50%;
    margin-right: 20px;
    border: 5px solid pink;

  }
  &-text {
    max-width: 390px;
    font-style: italic;
    h3 {
      font-size: 24px;
      
    }
  }
}
</style>
