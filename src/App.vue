<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<!-- <template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template> -->

<template>
  <div class="qrcode-generator">
    <h1>QR Code Generator</h1>
    <!-- <form class="qrcode-form" @submit.prevent="generateQRCode"> -->
    <form class="qrcode-form">
      <label for="qr-text">Enter text or URL:</label>
      <input type="text" id="qr-text" v-model="qrText" />
      <button type="submit">Generate QR Code</button>
    </form>
  </div>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        qrText: ''
      }
    }
  }
</script>


<style lang="scss">
.qrcode-generator {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;

  h1 {
    font-size: 2.5rem;
    margin-bottom: 2rem;
  }

  .qrcode-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 500px;
    width: 100%;
    margin: 0 auto;
    padding: 2rem;

    label {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }

    input {
      width: 100%;
      padding: 1rem;
      font-size: 1.5rem;
      margin-bottom: 1rem;
      border: none;
      border-radius: 0.5rem;
      background-color: #f1f1f1;
      color: #333;
      text-align: center;

      &:focus {
        outline: none;
        background-color: #fff;
        box-shadow: 0 0 5px #ccc;
      }
    }

    button {
      padding: 1rem 2rem;
      font-size: 1.5rem;
      border: none;
      border-radius: 0.5rem;
      background-color: #3498db;
      color: #fff;
      cursor: pointer;

      &:hover {
        background-color: #2980b9;
      }
    }
  }
}
</style>

