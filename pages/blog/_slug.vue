<template>
  <article>
    <div>
      <img
        :src="article.img"
        :alt="article.alt"
      >
      <div />
      <div>
        <NuxtLink to="/">
          <Logo />
        </NuxtLink>
        <div>
          <p>
            {{ formatDate(article.updatedAt) }}
          </p>
          <span>•</span>
          <p>{{ article.author.name }}</p>
        </div>
        <h1>
          {{ article.title }}
        </h1>
        <span v-for="(tag, id) in article.tags" :key="id">
          <NuxtLink :to="`/blog/tag/${tags[tag].slug}`">
            <span>
              {{ tags[tag].name }}
            </span>
          </NuxtLink>
        </span>
      </div>
      <div>
        <NuxtLink
          to="/"
        >
          All articles
        </NuxtLink>
        <a
          href="https://nuxtjs.org/blog/creating-blog-with-nuxt-content"
        >
          Tutorial
        </a>
        <AppSearchInput />
      </div>
    </div>
    <div>
      <h1>
        {{ article.title }}
      </h1>
      <p>{{ article.description }}</p>
      <p>
        Post last updated: {{ formatDate(article.updatedAt) }}
      </p>
      <!-- table of contents -->
      <nav>
        <ul>
          <li
            v-for="link of article.toc"
            :key="link.id"
          >
            <nuxtLink
              :to="`#${link.id}`"
            >
              {{ link.text }}
            </nuxtLink>
          </li>
        </ul>
      </nav>
      <!-- content from markdown -->
      <nuxt-content :document="article" />
      <!-- content author component -->
      <author :author="article.author" />
      <!-- prevNext component -->
      <PrevNext :prev="prev" :next="next" />
    </div>
  </article>
</template>
<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()
    const tagsList = await $content('tags')
      .only(['name', 'slug'])
      .where({ name: { $containsAny: article.tags } })
      .fetch()
    const tags = Object.assign({}, ...tagsList.map(s => ({ [s.name]: s })))
    const [prev, next] = await $content('articles')
      .only(['title', 'slug'])
      .sortBy('createdAt', 'asc')
      .surround(params.slug)
      .fetch()
    return {
      article,
      tags,
      prev,
      next
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
