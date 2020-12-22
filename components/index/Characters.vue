<template>
  <b-container>
    <AlignRowItems :class-name="['title', 'text']">
      <b-row align-h="center">
        <b-col class="text-center">
          <h2>得意な分野</h2>
          <hr />
        </b-col>
      </b-row>
      <b-row cols="1" cols-md="2" cols-lg="4">
        <b-col v-for="(item, key) in contents" :key="key">
          <img :src="item.image.url" :alt="item.image.src" class="w-100 my-2" />
          <h3 class="title my-3">
            <b>{{ item.title }}</b>
          </h3>
          <nuxt-content class="text my-2" :document="item" />
          <nuxt-link class="my-2" to="#">&gt; 詳しく見る</nuxt-link>
        </b-col>
      </b-row>
    </AlignRowItems>
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
