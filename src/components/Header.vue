<template>
  <header class="header">
    <div class="container">
      <div class="header-content">
        <a href="#" class="logo">
          <span>Light</span>
          <span>Fragance</span>
        </a>

        <nav class="menu">
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: 'Header'
});
</script>

<style lang="scss" scoped>
@import "../style/variaveis.scss";
@import "../style/functions.scss";

.header {
  box-shadow: $box-shadow-down;
  z-index: 100;
  padding: 10px;
      margin-bottom: 2px;
  &-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .logo {
      font-family: "MonteCarlo", cursive;
      font-size: 2rem;
      span {
        color: $color-black;
        &:last-child {
          color: pink;
        }
      }
    }
    .menu {
      ul {
        display: flex;
        li {
          padding: 14px;
        }
      }
    }
  }
}
</style>
