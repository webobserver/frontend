<template>
  <div class="home">
    <article>
      <img src="@/assets/apps.jpg" />
      <p>
        WebObserver is a web-scraping web based application that will enable you
        to keep track of your favourite websites and will allow you to find
        information you need faster.
      </p>
    </article>
    <article>
      <img src="@/assets/eagle.jpg" />
      <p>
        Want to keep track on prices of products you need? No problem! Get on
        and we'll make sure to keep you posted. It's only a matter of seconds to
        set it up!
      </p>
    </article>
    <article>
      <img src="@/assets/tree.png" />
      <p>
        Our platform is entirely written based on nodejs and vue which will
        guarantee that your websites will be scraped no matter what.
      </p>
    </article>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class Home extends Vue {}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@1,700&display=swap");

.home {
  flex-direction: column;
  display: flex;

  article {
    padding: 10px;
    display: flex;
    flex-direction: row;

    p {
      font-family: "Lato", sans-serif;
      margin: 20px;
      padding: 10px;
      font-size: 38px;
      text-align: center;
      display: flex;
      align-self: center;
    }

    img {
      height: 400px;
      border: solid black;
      border-radius: 15px;
    }
  }

  article:nth-child(even) {
    flex-direction: row-reverse;

    img {
      height: 400px;
    }
  }
}
</style>
