<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <CustomComponent :user="user"  />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import CustomComponent from '@/components/CustomComponent.vue';
import type { User } from './interfaces/User';

export default defineComponent({
  name: 'App',
  components: {
    CustomComponent
  },
  data(): {user:User}{
    return {
      user: {
        name: "Agustin",
        mail: "agus@gmail.com",
        age: 21,
        isLoggedIn: false
      }
    }
  }
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
