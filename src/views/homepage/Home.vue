<template>
  <div data-barba="wrapper" class="home">
    <nav-bar></nav-bar>
    <div class="planet">
      <img src="../../assets/jupiter.png" alt="">
    </div>
    <div class="info">
      <h1 class="title">
        Mars travel
      </h1>
      <h2>
        A human mission to marshas been the subject
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, non!
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem nisi dolores cumque distinctio fugiat amet porro voluptatum optio incidunt animi!
      </h2>
      <br>
      <button class="button is-primary">Get started</button>
      <br><br>
    </div>
    <div class="plus">
      <div class="card">
        <div class="card-image">
          <figure class="image is-48x48">
            <img src="../../assets/logo.png" alt="">
          </figure>
        </div>
          <div class="card-content">
            <div class="content">
              <h1>Space Travel</h1>
              <p>Read the latest spaceflight news </p>
            </div>
          </div>
      </div>
      <div class="card">
        <div class="card-image">
          <figure class="image is-48x48">
            <img src="../../assets/logo.png" alt="">
          </figure>
        </div>
          <div class="card-content">
            <div class="content">
              <h1>Traveller</h1>
              <p>Read the latest spaceflight news </p>
            </div>
          </div>
      </div>
    </div>
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

<style lang="scss" scoped>
  .planet{
    position: absolute;
    left: 60%;
    top: 15%;
    img{

    }
  }
  .info{
    h1, h2{
      color: white;
    }
    width: 50%;
    margin: 10% 0px 50px 10%;
  }
  .plus{
    display: flex;
    justify-content: start;
    margin: 0px 10%;
  }
  .card{
    background-color: rgba(70, 44, 105, 0.418);
    margin-right: 50px;
    padding: 10px;
    width: 200px;
    display: flex;
    justify-content: space-around;
    flex-direction: column;
    align-items: center;
    h1{
      color: white;
    }
    p{
      color: rgba(245, 245, 245, 0.555);
    }
  }
</style>
