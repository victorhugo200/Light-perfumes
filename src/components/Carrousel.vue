<template>
  <slick ref="slick" :options="slickOptions">
    <div class="slide slide--1"></div>
    <div class="slide slide--2"></div>
    <div class="slide slide--3"></div>
  </slick>
</template>

<script lang="ts">
import Slick from "vue-slick";

export default {
  name: "Carrousel",
  components: {
    Slick
  },
  data() {
    return {
      slickOptions: {
        slidesToShow: 1,
        prevArrow: false,
        nextArrow: false,
        autoplay: true,
        infinite: true,
        dots: true,
        autoplaySpeed: 3000
      },
      list: [1, 2, 3]
    };
  },
  methods: {
    setClass(index: number) {
      const classe = `slide slide--${index}`;
      switch (index) {
        case 0:
          return classe;
        case 1:
          return classe;
        case 2:
          return classe;
        default:
          return "";
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.bgc {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
//  Slide
.slide {
  height: 500px;
  position: relative;

  @extend .bgc;
  &--1 {
    background-image: url("../assets/img/perfume-1.jpg");
  }
  &--2 {
    background-image: url("../assets/img/perfume-2.jpg");
  }
  &--3 {
    background-image: url("../assets/img/perfume-3.jpg");
  }
}

::v-deep .slick-dots {
	display: flex;
	justify-content: center;
	margin: 0;
	padding: 1rem 0;
    position: absolute ;
    bottom: 10%;
    left: 50%;
	
	list-style-type: none;
	
		li {
			margin: 0 0.25rem;
		}
	
		button {
			display: block;
			width: 1rem;
			height: 1rem;
			padding: 0;
			
			border: none;
			border-radius: 100%;
			background-color: #eaeaea94;
			
			text-indent: -9999px;
		}
	
		li.slick-active button {
			background-color: white;
		}
	
}
</style>
