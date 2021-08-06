<template>
  <div class="content">
    <main class="home">
      <div class="home-text">
        <h1 class="title">{{ info.title }}</h1>
        <p class="subtitle">
          {{ info.subtitle }}
        </p>

        <button class="btn">Shop now</button>
      </div>
      <div class="home-carrousel">
        <Carrousel />
      </div>
    </main>
    <section class="about">
      <div class="container">
        <h2 class="about_title">Why Ever Bloom is so unique</h2>
        <div class="about-list">
          <div class="item" v-for="(item, index) in about.list" :key="index">
            <InfoFlor :isRight="item.isRight" :title="item.title" :text="item.text" :img="item.url" />
          </div>
        </div>
      </div>
    </section>
    <section class="everbloom">
    <div class="container">
      <h2 class="title">Why Ever Blom is so unique </h2>

      <div class="content">
        <div class="content-text">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corporis maiores harum iusto esse praesentium. Eos, deleniti amet. Molestias eveniet repellendus asperiores unde beatae architecto dolore, numquam nam magnam odit iure!
          </p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod obcaecati tempore ex molestiae fugiat eius repellendus cum iure exercitatio. </p>
        </div>
        <div class="content-img">
          <img src="../assets/img/perfume-4.png" alt="">
        </div>
      </div>
    </div>
  </section>
  </div>
</template>

<script lang="ts">
import Slick from "vue-slick";
import Carrousel from "../components/Carrousel.vue";
import InfoFlor from "../components/InfoFlor.vue";

export default {
  name: "Home",
  components: {
    Slick,
    Carrousel,
    InfoFlor
  },
  data() {
    return {
      slickOptions: {
        slidesToShow: 1,
        prevArrow: false,
        nextArrow: false,
        autoplay: true,
        autoplaySpeed: 3000
      },
      info: {
        title: "Bloom every moment",
        subtitle:
          " Just one drop of this delicate floral arama fills the space around you"
      },
      about: {
        title: "The moment of happines",
        list: [
          {
            title: 'Usin clear melted water',
            text: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam
                incidunt dolores, maxime placeat, quibusdam eaque rerum cum
                perspiciatis cupiditate`,
            isRight: false,
            url: '/img/flor-1.5e046949.jpg'
          },
          {
            title: 'Usin clear melted water',
            text: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam
                incidunt dolores, maxime placeat, quibusdam eaque rerum cum
                perspiciatis cupiditate`,
            isRight: true,
            url: '/img/flor-2.3f4b8eaf.jpg'
          },
          {
            title: 'Usin clear melted water',
            text: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam
                incidunt dolores, maxime placeat, quibusdam eaque rerum cum
                perspiciatis cupiditate`,
            isRight: false,
            url: '/img/flor-3.21fd597d.jpg'
          },
          
        ]
      }
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../style/variaveis.scss";
@import "../style/functions.scss";

.home {
  padding: 60px 30px;
  height: 500px;
  position: relative;
  overflow: hidden;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  &-text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    z-index: 30;
    padding: 40px 0;
    max-width: 1024px;
    width: 100%;
    margin: 0 auto;

    .title {
      font-size: 62px;
      font-weight: normal;
    }

    .subtitle {
      font-size: 24px;
      max-width: 580px;
      margin-top: 32px;
      line-height: 1.2;
    }
    .btn {
      width: 190px;
      background-color: $color-pink;
      padding: 10px;
      border-radius: 20px;
      text-align: center;
      color: white;
      font-size: 18px;
      margin-top: 40px;
      cursor: pointer;
      border: 1px solid $color-pink;
    }
  }

  &-carrousel {
    width: 60%;
    top: 0;
    right: 0;
    position: absolute;
  }
}

// About

.about {
  padding: 130px 30px;
  &_title {
    font-size: 52px;
    line-height: 1;
    max-width: 500px;
    text-align: start;
  }

  &-list {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-bottom: 60px;
  }
}

.everbloom {
  padding: 100px 30px;
  background: radial-gradient(#ffffff47, #ff839957);

  .title {
    font-size: 52px;
    max-width: 400px;
  }
  .content {
    display: flex;
    justify-content: space-between;

    &-text {
      flex-grow: 1;
      width: 40%;
    }
    &-img {
      flex-grow: 2;
    }
  }
}
</style>
