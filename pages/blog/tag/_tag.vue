<template>
  <div>
    <div>
      <img
        :src="tag.img"
        :alt="tag.name"
      >
    </div>
    <div>
      <NuxtLink to="/">
        <Logo />
      </NuxtLink>
      <div>
        <div>
          <h1>
            {{ tag.name }}
          </h1>
          <p>
            {{ tag.description }}
          </p>

          <nuxt-content :document="tag" />
        </div>
      </div>
    </div>
    <div>
      <NuxtLink
        to="/"
      >
        <p>
          Back to All Articles
        </p>
      </NuxtLink>
      <h3>
        Articles tagged {{ tag.name }}:
      </h3>
      <ul>
        <li
          v-for="article in articles"
          :key="article.slug"
        >
          <NuxtLink
            :to="{ name: 'blog-slug', params: { slug: article.slug } }"
          >
            <img
              v-if="article.img"
              :src="article.img"
              :alt="article.alt"
            >

            <div>
              <h2>
                {{ article.title }}
              </h2>
              <p>{{ article.description }}</p>
              <p>
                {{ formatDate(article.updatedAt) }}
              </p>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const tags = await $content('tags')
      .where({ slug: { $contains: params.tag } })
      .limit(1)
      .fetch()
    const tag = tags.length > 0 ? tags[0] : {}
    const articles = await $content('articles', params.slug)
      .where({ tags: { $contains: tag.name } })
      .sortBy('createdAt', 'asc')
      .fetch()
    return {
      articles,
      tag
    }
  },
  methods: {
    formatDate (date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  }
}
</script>
