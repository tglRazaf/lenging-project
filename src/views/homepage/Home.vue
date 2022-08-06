<template>
  <div data-barba="wrapper" class="home">
    <nav-bar></nav-bar>
    <header data-barba="container">
      <div class="content">
        <h1>This page was revealed<br />using a simple CSS <br />clip-path transition</h1>
        <p>Now lets show some cover screen.</p>
        <router-link to="/">Cover Transition</router-link>
      </div>
    </header>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';// @ is an alias to /src
import NavBar from '@/components/NavBar.vue';
import barba from "@barba/core";
import gsap from 'gsap';

@Options({
  components: {
    NavBar
  },
})
export default class Home extends Vue {
  
  mounted(): void{
    barba.init({
      transitions: [
        {
          name: 'opacity-transition',
          leave: (data) => {
            gsap.to(data.current.container, {opacity: 0, width: 50})
          },
          enter: (data)=> {
            gsap.from(data.current.container, {opacity: 0, width: 50})
          },
        }
      ]
    })
  }
}
</script>
