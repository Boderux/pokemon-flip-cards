<script>
import MainScreen from "./components/MainScreen.vue";
import InteractScreen from "./components/InteractiveScreen.vue";
export default {
  data() {
    return {
      showMainScreen: true,
      showInteractScreen: false
    };
  },
  components: {
    MainScreen,
    InteractScreen
  },
  methods: {
    onHandle(block) {
      this.showInteractScreen = true;
      this.showMainScreen = false;
      console.log(block);
    }
  }
};
</script>

<template>
  <main-screen v-if="showMainScreen" @onStart="onHandle($event)"></main-screen>
  <interact-screen v-if="showInteractScreen"></interact-screen>
</template>

