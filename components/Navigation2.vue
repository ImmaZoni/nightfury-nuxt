<template>
    <v-navigation-drawer
      app
      clipped
      permanent
      mini-variant
      expand-on-hover>
      <!-- -->

      <v-list nav dense>
       <div v-for="(link, i) in links" :key="i">
        
        <v-list-item
            v-if="!link.subLinks"
            :to="link.to"
            :active-class="color"
            avatar
            class="v-list-item"
        >
            <v-list-item-icon>
                <v-icon>{{ link.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-title v-text="link.text" />
        </v-list-item>

        <v-list-group
            v-else
            :key="link.text"
            no-action
            :prepend-icon="link.icon"
            :value="false"
        >
            <template v-slot:activator>
              <v-list-item-title>{{ link.text }}</v-list-item-title>
             </template>

            <v-list-item
                v-for="sublink in link.subLinks"
                :to="sublink.to"
                :key="sublink.text"
            >
                <v-list-item-icon>
                  <v-icon>{{ sublink.icon }}</v-icon>
                </v-list-item-icon>
                <v-list-item-title>{{ sublink.text }}</v-list-item-title>

            </v-list-item>
        </v-list-group>
    </div>

      </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
links: [
    {
        to: '/',
        icon: 'mdi-home',
        text: '',
        title: 'Webpage home'
    },
    {
        icon: 'mdi-folder',
        text: 'Make a Difference',
        title: 'How to make a difference',
        subLinks: [
            {
                to: '/Adopt',
                icon: '',
                text: 'Adopt',
                title: 'Adopt an Animal'
            },
            {
                to    : '/Foster',
                icon  : '',
                text : 'Foster',
                title: 'Foster an Animal'
            },
        ]
    },
    {
        icon: 'mdi-folder',
        text: 'Care & Rescue',
        title: 'Care & Rescue resources',
        subLinks: [
            {
                to: '/Resources',
                icon: '',
                text: 'Resources',
                title: 'Various helpful resources'
            },
            {
                to    : '/Information',
                icon  : '',
                text : 'Information',
                title: 'Animal Information'
            },
        ]
    },
    {
        icon: 'mdi-folder',
        text: 'Sanctuary',
        title: 'Our Sanctuary',
        subLinks: [
            {
                to: '/Animals',
                icon: '',
                text: 'Animals',
                title: 'Our Animals'
            },
            {
                to    : '/About-Us',
                icon  : '',
                text : 'About Us',
                title: 'About Our Sanctuary'
            },
        ]
    },
    {
        to: '/Blog',
        icon: 'mdi-folder',
        text: 'Blog',
        title: 'Our blog'
    },
    {
        href: 'https://www.facebook.com',
        icon: 'mdi-email',
        text: '',
        title: 'Email-Us'
    },
    {
        href: 'https://www.facebook.com',
        icon: 'mdi-facebook',
        text: '',
        title: 'Facebook'
    },
    {
        href: 'https://www.twitter.com',
        icon: 'mdi-twitter',
        text: '',
        title: 'Twitter'
    },
    {
        href: 'https://wwww.instagram.com',
        icon: 'mdi-Instagram',
        text: '',
        title: 'Instagram'
    },
]
  })
}
</script>