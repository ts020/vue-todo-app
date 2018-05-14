<template>
  <div id="app">
    <div>
          <input type="text" v-model="inputTitle">
          <button @click="addItem">追加</button>
      </div>
      <ul>
          <item v-for="(item, index) in items" :item="item" :key="index"></item>
      </ul>
      
  </div>
</template>
<script>
import Item from "./Item.vue";
export default {
  name: "app",
  components: { Item },
  data() {
    const items = [];
    for (var i = 0; i < 1750; i++) {
      items.push({ is_do: false, title: "タスク" + i });
    }
    return {
      inputTitle: "",
      items: items
    };
  },
  methods: {
    addItem() {
      this.items.push({
        title: this.inputTitle,
        is_do: false
      });
    }
  }
};
</script>
