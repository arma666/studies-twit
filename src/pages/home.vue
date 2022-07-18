<template lang="html">
  <p>hello vew</p>
  <div class="card_wrapper" v-for="item in items" :key="item.id">
    <Card :name="item.lvl + ' lvl'" :title="item.title" />
  </div>
</template>

<script>
import Card from "@/components/UI/card";
export default {
  components: {
    Card,
  },
  data() {
    return {
      items: [
        {
          id: 1,
          title: "Archer",
          descr: "archer archer archer archer",
          lvl: 4,
        },
        {
          id: 2,
          title: "Wizard",
          descr: "Wizard Wizard Wizard Wizard",
          lvl: 5,
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped></style>
