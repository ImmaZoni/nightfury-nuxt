<template>
    <v-layout justify-center>
        <v-toolbar app dark class="hidden-xs-and-down">
            <v-spacer></v-spacer>
            <v-toolbar-items>
                <v-btn nuxt icon>
                    <nuxt-link to="/">
                        <v-icon>
                            mdi-home
                        </v-icon>
                    </nuxt-link>
                </v-btn>
                <v-btn
                    plain
                    v-for="link in links"
                    :key="link.text"
                    :to="link.to"
                >
                        {{ link.text }}
                </v-btn>
                <v-btn
                    plain
                    
                    >
                </v-btn>
            </v-toolbar-items>
        </v-toolbar>
    </v-layout>
</template>
<script>
export default {
    data: () => ({
        links: [
        {
            text: '',
            sub: 'Webpage Home',
            icon: 'mdi-home',
            to: '/'
        },
        {
            text: 'Make a Difference',
            sub: 'How to Make a Difference',
            icon: 'mdi-folder',
            subLinks: [
            {
                text: 'Adopt',
                sub: 'Adopt an Animal',
                icon: '',
                to: '/Adopt'
            },
            {
                text: 'Foster',
                sub: 'Foster an Animal',
                icon: '',
                to: '/Foster' 
            },
            ]
        },
        {
            text: 'Care & Rescue',
            sub: 'Care and rescue resources',
            icon: 'mdi-folder',
            subLinks: [
            {
                text: 'Resources',
                sub: 'Various helpful resources',
                icon: '',
                to: '/Resources'
            },
            {
                text: 'Information',
                sub: 'Animal Information',
                icon: '',
                to: '/Information'
            },
            ]
        },
        {
            text: 'Sanctuary',
            sub: 'Our Sanctuary',
            icon: 'mdi-folder',
            subLinks: [
            {
                text: 'Animals',
                sub: 'Our Animals',
                icon: '',
                to: '/Animals'
            },
            {
                text: 'About Us',
                sub: 'About Our Sanctuary',
                icon: '',
                to: '/About-Us' 
            },
            ]
        },
        {
            text: 'Blog',
            sub: 'Our Sanctuary',
            icon: 'mdi-blog',
            to: '/Blog'
        }
        ],
        urls: [
        {
            sub: 'Email Us',
            icon: 'mdi-email',
            href: 'https://www.Test.com'
        },
        {
            sub: 'Facebook',
            icon: 'mdi-facebook',
            href: 'https://www.facebook.com'
        },
        {
            sub: 'Twitter',
            icon: 'mdi-twitter',
            href: 'https://www.twitter.com'
        },
        {
            sub: 'Instagram',
            icon: 'mdi-instagram',
            href: 'https://www.instagram.com'
        },
        ]
    })
}
</script>