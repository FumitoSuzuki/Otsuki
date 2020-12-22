<template>
  <b-container>
    <b-row class="title my-5">
      <b-col class="text-center">
        <h2>ニュース</h2>
      </b-col>
    </b-row>
    <b-row
      v-for="(item, key) in contents"
      :key="key"
      align-v="center"
      class="line mb-3"
    >
      <b-col md="2">
        <p>{{ item.date }}</p>
      </b-col>
      <b-col md="3">
        <p>{{ item.category }}</p>
      </b-col>
      <b-col md="7">
        <nuxt-content :document="item" />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  props: {
    contents: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style scoped>
.title {
  border-bottom: 1px solid #333;
}
.line {
  border-bottom: 1px solid #ccc;
}
</style>
