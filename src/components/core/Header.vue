<template>
  <div class="header">
    <app-nav-drawer :drawer="drawerValue"></app-nav-drawer>
    <app-nav-bar :drawer="drawerValue" @toggle="toggleDrawerHandler($event)"></app-nav-bar>
  </div>
</template>

<script>
import AppNavDrawer from "./NavDrawer.vue";
import AppNavBar from "./NavBar.vue";

export default {
  data: function() {
    return {
      drawerValue: true
    };
  },
  methods: {
    toggleDrawerHandler(value) {
      this.drawerValue = value;
    }
  },
  components: {
    AppNavDrawer,
    AppNavBar
  }
};
</script>

<style scoped lang="scss">
</style>