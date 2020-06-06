<template>
  <div id="registration-form">
    <h2>Register</h2>
    <form @submit="verifyForm">
      <label>Email: </label> <input v-model="email" type="email" />
      <label>Password: </label> <input v-model="password" type="password" />
      <label>Repeat Password: </label>
      <input v-model="repeatedPassword" type="password" />
      <button class="button" type="submit">Register</button>
    </form>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class Register extends Vue {
  email: string | undefined;
  password: string | undefined;
  repeatedPassword: string | undefined;
  verifyForm(): void {
    if (this.email && this.password && this.repeatedPassword) {
      if (this.password === this.repeatedPassword) {
        alert("Send post message!");
      } else {
        alert("Password are not the same!");
      }
    } else {
      alert("Please fill up all of the inputs!");
    }
  }
}
</script>

<style scoped lang="scss">
@import "@/scss/_variables.scss";
#registration-form {
  text-align: center;
  h2 {
    font-size: 40px;
  }
  form {
    display: grid;
    grid-template-columns: 30% 20% 20% 30%;
    font-family: "Lato", sans-serif;
    font-size: 24px;
    label {
      margin: 10px;
      align-self: center;
      grid-column: 2;
    }
    input {
      padding: 10px;
      margin: 10px;
      font-size: 24px;
    }
    button {
      grid-column-start: 2;
      grid-column-end: 4;
      align-self: center;
    }
  }
}
</style>
