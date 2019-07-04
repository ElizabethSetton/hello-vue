<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <app-id-card></app-id-card>
  </div>
</template>

<script>
  import idCard from './components/idCard/idCard.vue'
  import header from './components/header/header.vue'
  import infoProjects from './components/infoProjects/infoProjects.vue'
  import galleryProjects from './components/galleryProjects/galleryProjects.vue'
  import infoDiploma from './components/infoDiploma/infoDiploma.vue'
  import galleryDiploma from './components/galleryDiploma/galleryDiploma.vue'
  import infoPersonal from './components/infoPersonal/infoPersonal.vue'
  import footer from './components/footer/footer.vue'

  export default {
    name: 'app',
    components: {
      'app-id-card': idCard,
      'app-header': header,
      'app-info-projects': infoProjects, 
      'app-gallery-projects': galleryProjects,
      'app-info-diploma': infoDiploma, 
      'app-gallery-diploma': galleryDiploma,
      'app-info-personal': infoPersonal,
      'app-footer': footer
    }
}
</script>

<style lang="scss">
/////////// COLORS ///////////

$color-purple-light: #c9cfe5;
$color-purple-lighter: #a397b7;
$color-purple-dark: #a691b6;

$color-heading: #6f506f;

$color-border: 1px solid #c9cfe5;
$color-background: #f9f7f6;


/////////// TYPOGRAPHY ///////////

$font-size-smallest: 1rem;
$font-size-small: 1.3rem;
$font-size-medium2: 1.4rem;
$font-size-medium1: 1.6rem;
$font-size-big: 1.9rem;

/////////// GENERAL ///////////

$general-box-shadow: 0px 5px 8px 0px rgba(0, 0, 0, 0.14);





#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

@mixin respond($breakpoint) {
    @if $breakpoint == phone-small {
        @media (max-width: 33.5em) {@content}; //540px
    }
    @if $breakpoint == phone-medium {
        @media (max-width: 38.5em) {@content}; //600px
    }
    @if $breakpoint == phone-big {
        @media (max-width: 43.8em) {@content}; //700px
    }
    @if $breakpoint == tab-port {
        @media (max-width: 56.25em) {@content}; //900px
    }
    @if $breakpoint == tab-land {
        @media (max-width: 75em) {@content}; //1200px
    }
    @if $breakpoint == big-desktop {
        @media (min-width: 112.5em) {@content}; //1800px
    }

}
</style>
