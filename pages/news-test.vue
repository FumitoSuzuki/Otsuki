<template>
  <section id="main">
    <!-- <b-container v-pre>
      <b-row>
        <b-col class="text-center">
          <h1>News Test</h1>
        </b-col>
      </b-row>
    </b-container> -->
    <News :contents="news" />
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const news = await $content('news').sortBy('date', 'desc').fetch()
    return {
      news,
    }
  },
}
</script>
