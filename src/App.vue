<template>
  <div id="app">
    <h3>打开 console 或者 vue 插件查看性能差异</h3>
    <normal-component />
    <slot-component />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import NormalComponent from "./components/NormalComponent.vue";
import SlotComponent from "./components/SlotComponent.vue";

@Component({
  components: {
    NormalComponent,
    SlotComponent
  }
})
export default class App extends Vue {}
</script>

<style>
#app {
  display: flex;
  justify-content: space-around;
}

* {
  text-align: center;
}
</style>