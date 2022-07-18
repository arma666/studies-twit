<template lang="html">
  <div class="card_wrapper" v-for="item in items" :key="item.id">
    <Card :name="item.lvl + ' lvl'" :title="item.title" :imgUrl="item.img">
      {{ item.descr }}
    </Card>
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
          img: require("/assets/img/archer.png"),
          descr: "archer archer archer archer",
          lvl: 4,
        },
        {
          id: 2,
          title: "Wizard",
          img: require("/assets/img/wizard.png"),
          descr: "Wizard Wizard Wizard Wizard",
          lvl: 5,
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped></style>
