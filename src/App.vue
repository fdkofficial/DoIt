<template>
  <div class="container1">
    <router-view />
  </div>
    <footer>
      <div class="card">
        <TabMenu :model="items" />
      </div>
    </footer>
</template>
<script setup>
import { ref } from "vue";

const items = ref([
    {
        label: 'Todo',
        icon: 'pi pi-fw pi-home',
        to: '/todo'
    },
    {
        label: 'Alarm',
        icon: 'pi pi-fw pi-calendar',
        to: '/'
    },
    {
        label: 'Chat',
        icon: 'pi pi-fw pi-pencil',
        to: '/edit'
    }
]);

</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

/* For Mobile Portrait View */
.container1{
  margin-top: 5px;
}
@media screen and (max-device-width: 480px)
    and (orientation: portrait) {
    .container1 {
      height: 765px;
    }
}

@media screen and (max-device-width: 380px)
    and (orientation: portrait) {
    .container1 {
      height: 580px;
    }
}


 
</style>