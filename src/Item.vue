<template>
    <li :class="{ 'is-do': item.is_do }" @click="done(item)">
    <span>{{ item.title }}-1 </span>
    <span>{{ item.title }}-2 </span>
    <span>{{ item.title }}-3 </span>
    <span>{{ item.title }}-4 </span>
    <span>{{ item.title }}-5 </span>
    </li>
</template>
<script>
export default {
  props: ["item"],
  methods: {
    done(item) {
      item.is_do = !item.is_do;
    }
  }
};
</script>
<style lang="scss" scoped>
li {
  cursor: pointer;
}
li.is-do {
  text-decoration: line-through;
}
</style>
