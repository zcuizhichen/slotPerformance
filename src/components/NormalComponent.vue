<template>
  <div>
    <button @click="count++">item add</button>
    <div v-for="item in count" :key="item">
      <Item :item="item"></Item>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Item from "./Item.vue";

@Component({
  components: {
    Item
  }
})
export default class Normal extends Vue {
  count: number = 5;
}
</script>