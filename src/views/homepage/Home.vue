<template>
  <div data-barba="wrapper" class="home">
    <nav-bar></nav-bar>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';// @ is an alias to /src
import NavBar from '@/components/NavBar.vue';
import LottieAnimation from "lottie-vuejs/src/LottieAnimation.vue";

@Options({
  components: {
    NavBar,
    LottieAnimation
  },
})
export default class Home extends Vue {
  isLoading = true
  mounted():void{
    console.log('start');
  }
}
</script>
