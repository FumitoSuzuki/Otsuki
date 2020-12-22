<template>
  <section id="main">
    <FixidAspectBox
      :aspect-x="983.33"
      :aspect-y="211.34"
      :aspect-md-x="1"
      :aspect-md-y="2"
    >
      <Introduction class="text-center">
        <template #body>
          <h1>伝わる。勝つ。</h1>
        </template>
      </Introduction>
    </FixidAspectBox>
    <article>
      <Characters :contents="characters" class="my-5" />
      <Topics :rows="topics" />
      <Others :contents="others" class="my-3" />
    </article>
    <aside class="bg-info py-5">
      <Information />
    </aside>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const intro = await $content('introduction').fetch()
    const leadcopy = await $content('leadcopy').fetch()
    const characters = await $content('characters').sortBy('slug').fetch()
    const topics = await $content('topics').sortBy('slug').fetch()
    const others = await $content('others').fetch()
    return {
      intro,
      leadcopy,
      characters,
      topics: [topics.splice(0, 2), topics],
      others,
    }
  },
}
</script>

<style>
#main {
  background-color: white;
}
</style>
