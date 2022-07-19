<template lang="html">
  <div class="card_wrapper" v-for="item in items" :key="item.id">
    <Card :name="item.lvl + ' lvl'" :title="item.title" :imgUrl="item.img">
      {{ item.descr }}
    </Card>
  </div>
</template>

<script>
import items from "@/seeders/items.js";
import Card from "@/components/UI/card";
export default {
  components: {
    Card,
  },
  data() {
    return {
      items: items,
    };
  },
};
</script>

<style lang="css" scoped></style>
