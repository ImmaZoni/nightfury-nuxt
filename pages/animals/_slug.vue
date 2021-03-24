<template>
  <article>
    
    <h1>{{ animal.title }}</h1>
    <h2>Author: {{ animal.author }}</h2>
    <p>{{ animal.description }}</p>
    <img :src="animal.img" :alt="animal.alt" />
    <p>Article last updated: {{ formatDate(animal.updatedAt) }}</p>
    <nav>
      <ul>
        <li v-for="link of animal.toc" :key="link.id">
          <NuxtLink :to="`#${link.id}`">{{ link.text }}</NuxtLink>
        </li>
      </ul>
    </nav>
    <nuxt-content :document="animal" />
  </article>
</template>
<style>
  .nuxt-content h2 {
    font-weight: bold;
    font-size: 28px;
  }
  .nuxt-content h3 {
    font-weight: bold;
    font-size: 22px;
  }
  .nuxt-content p {
    margin-bottom: 20px;
  }
  
</style>
<script>
  export default {
    async asyncData({ $content, params }) {
      const animal = await $content('animals', params.slug).fetch()

      return { animal }
    },
    methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
 }
}
</script>
