<template>
  <div id="nav">
    <ul class="nav-links">
      <li class="links">
        <router-link to="/">Home</router-link>
      </li>
      <li v-for=""></li>
    </ul>
     
      <router-link to="/brazil">Brazil</router-link>
      <router-link to="/hawaii">Hawaii</router-link>
      <router-link to="/jamaica">Jamaica</router-link>
      <router-link to="/panama">Panama</router-link>
    </div>
</template>

<style scoped>
#nav {
  display: flex;
  align-items: center;
  padding: 30px;

}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0 10px;
}

#nav a.vue-school-active-class {
  color: #ab26ab;
}
</style>