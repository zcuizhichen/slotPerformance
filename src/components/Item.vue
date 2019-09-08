<template>
  <div>{{ item }}</div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Item extends Vue {
  @Prop(Number) readonly item;

  updated() {
    console.log("Update Item ");
  }
}
</script>