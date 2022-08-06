<template>
  <div data-barba="wrapper" class="about">
    <header data-barba="container" class="is-clip" data-barba-namespace="clip" data-background="#161636">
      <div class="transition">
        <h2>Cover Screen</h2>
      </div>
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
import barba from "@barba/core";

@Options({
  components: {
  },
})
export default class About extends Vue {
  
  mounted(): void{
    barba.init({
      transitions: [
        {
          name: 'clip',
          sync: true,
          leave: () => {
            console.log('leave');
          },
          enter: () => {
            console.log('enter');
          },
          once(){
            console.log('clip');
          }
        }
      ]
    })
  }
}
</script>

<style lang="scss" scoped>
  .is-clip{
    background-color: #161636; 
  }

  .clip-enter {
    clip-path: circle(0%);
  }
  .clip-enter-active {
      position: absolute;
      top: 0;
      z-index: 2;
  }
  .clip-leave-active,
  .clip-enter-active {
      transition: all 0.75s var(--easing);
  }
  .clip-enter-to {
      clip-path: circle(75%);
  }
  .clip-leave {
      opacity: 1;
  }
  .clip-leave-to {
      opacity: 0;
  }
.content {
  transition: all 0.3s ease-out;
  opacity: 1;
  transform: translateY(0);
}

.transition {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-color: #c8cc98;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: translateY(-100%);
  z-index: 1;

  > h2 {
    font-size: 40px;
    color: #202020;
  }
}
</style>