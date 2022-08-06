<template>
  <div id="nav">
  <router-view v-slot="{ Component }">
  <transition name="fade" appear mode="out-in">
    <component :is="Component" />
  </transition>
  </router-view>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-image: url('./assets/space-travel.png');
}

.fade-enter-active{
  transition: 2s;
}
.fade-leave-active{
  transition: 0.5s;
}
.fade-leave-to, .fade-enter{
  opacity: 0;
  transform:  translateX(50px);
}

</style>
