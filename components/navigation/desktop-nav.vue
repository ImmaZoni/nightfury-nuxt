<template>
  <div>
    <v-menu
      v-for="group in groups"
      :key="group.title"
      v-model="group.active"
      attach="#navbar"
      :prepend-icon="group.icon"
      transition="slide-y-transition"
      offset-y
      bottom
      eager
    >
      <template #activator="{ on, attrs }">
        <div>
          <v-btn v-bind="attrs" v-on="on">
            {{ group.title }}
          </v-btn>
        </div>
      </template>
      <v-list>
        <v-list-item
          v-for="child in group.items"
          :key="child.title"
          nuxt
          :to="child.to"
        >
          <v-list-item-content>
            <v-list-item-title v-text="child.title" />
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          v-model="item.active"
          :prepend-icon="item.icon"
          nuxt
          :to="item.to"
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
export default {
  data: () => ({
    groups: [
      {
        icon: '',
        items: [
          { title: 'Adopt', to: '/adopt' },
          { title: 'Foster', to: '/foster' },
          { title: 'Donate', to: '/donate' }
        ],
        title: 'Make A Difference'
      },
      {
        icon: '',
        items: [
          { title: 'Resources', to: '/resources' },
          { title: 'Animal Information', to: 'animal-information' }
        ],
        title: 'Care & Rescue'
      },
      {
        icon: '',
        items: [
          { title: 'Our Animals', to: 'our-animals' },
          { title: 'About Us', to: 'about-us' }
        ],
        title: 'Our Sanctuary'
      }
    ],
    items: [
      {
        icon: '',
        title: 'Blog',
        to: '/blog'
      }]
  })
}
</script>
