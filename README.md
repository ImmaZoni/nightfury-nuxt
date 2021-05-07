# Nightfury-Nuxt

**This is the private in development repository for The Circle of Life Animal Sanctuary**

### Built With
* [Vue.js](https://vuejs.org/)
* [Nuxt.js](https://nuxtjs.org/)
* [Vuetify.js](https://vuetifyjs.com/en/)

The main goal of this webpage is to properly display our non-profit organizations intentions, goals, and animal in a clear, consise, and beautiful manner.

Current Developmental Objectives

* Navigation Bar - Dynamic with Json format from <script> portion of .vue components
  * Dropdown menu needs to be properly displayed and accounted for within tabular i18n standards this doable with <menu>
  * Proper implementation with dynamic breakpoints and a hamburger mobile menu.
  * Sylization of navigation bar

* Footer - Footer needs to be updated and correlated within canva design (feel free to mess with it making it feel right)

* Loading animation for pre-render of images, we were thinking our logo with the outer paws *walking* around.

* Implement the predisnged webpages we have into layouts, and components as needed
  * For context, the footer is a component that can be re-added to the webpage over and over again very easily, we will want to build most of the site with components mostly for things we will be reusing during the lifecycle of the website. 
  * Layouts are the exact pages and how they are configured, home, blog, donate, are all layouts. NOTE: Views are the technical page but as it stands the layout is where we will *build* the structure of the page.













Our secondary goals are to ensure this webpage maintains a dynamic approach to content and loading of assets to ensure an enjoyable experience. 

We would like to focus user interaction to as many individuals as possible with some of the following features. 
* Full integration with ALL disabliity  accesbility features.
    * Text-to-Speach
    * Speach-to-Text
    * Closed Captions when needed
    * High Contrast color themes
    * Blind touch interaction
    

* Optional dyslexic friendly font
* Optional 


## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
