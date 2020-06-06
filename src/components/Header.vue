<template>
  <header>
    <h1>WebObserver</h1>
    <nav>
      <router-link class="button" to="/">Home</router-link>
      <router-link class="button" to="/about">About</router-link>
      <router-link class="button" to="/login">Login</router-link>
      <router-link class="button" to="/register">Register</router-link>
    </nav>
  </header>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class Header extends Vue {}
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
@import "@/scss/_variables.scss";
header {
  display: grid;
  grid-template-columns: 30% 70%; //TODO change on mobile
  background: #76b852; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #8dc26f,
    #76b852
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #8dc26f,
    #76b852
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

  width: 100%;

  h1 {
    font-family: "Pacifico", cursive;
    font-size: 48px;
    margin: 10px;
  }

  nav {
    text-align: right;
    font-size: 24px;
    align-items: center;
    justify-content: flex-end;
    display: flex;

    /* a {
                transition: background-color 1s, color 1s, border-color 1s;
                margin: 10px;
                display: inline-block;
                background-color: rgba(61, 100, 41, 0.7);
                border: solid black;
                border-radius: 15px;
                padding: 10px;
                color: black;
                text-decoration: none;
            }

            a:hover {
                background-color: rgba(61, 100, 41, 0.3);
                color: white;
                border-color: white;
            }*/
  }
}
</style>
