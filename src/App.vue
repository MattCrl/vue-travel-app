<template>
  <div id="app">
    <TheNavigation />
    <Transition name="slide" mode="out-in">
        <router-view :key="$route.path" />
    </Transition>
  </div>
</template>

<script>
import TheNavigation from "@/components/TheNavigation"

export default {
  components: {
    TheNavigation
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/* Slide transitions */
.slide-enter-active, 
.slide-leave-active {
  transition: opacity 0.3s, transform 0.3s;
}

.slide-enter, 
.slide-leave-to {
  opacity: 0;
  transform: translateX(-5%);
}

/* MoveUp Transitions */
.moveUp-enter-active {
  animation: fadeIn 1s ease-in;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  50% {
    opacity: 0.5;
  }

  100% {
    opacity: 1;
  }
}

.moveUp-leave-active {
  animation: moveUp 0.3 ease-in;
}

@keyframes moveUp {
  0% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(-400px);
  }
}

/* Fade transitions */
.fade-enter-active, .fade-leave-active {
  transition: opacity 1s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}

</style>
