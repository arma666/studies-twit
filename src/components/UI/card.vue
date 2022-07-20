<template lang="html">
  <div class="card">
    <div v-if="imgUrl" class="card-img__wrapper">
      <img class="card-img" :src="imgUrl" :alt="title" />
    </div>
    <span class="card-name">{{ name }}</span>
    <span class="card-title">{{ title }}</span>
    <div class="card-body">
      <slot></slot>
      <div class="">
        <router-link v-if="link" :to="link">go</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    imgUrl: {
      type: String,
    },
    link: {
      type: String,
    },
  },
};
</script>

<style lang="css" scoped></style>
