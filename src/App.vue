<template>
  <div id="app">
    <img v-bind:src="image.source" v-bind:alt="image.alternate_text">
    <app-header :message="msg"></app-header>
    <h1>{{ msg }}</h1>
    <button type="button" @click="changeHeading">change heading</button>
    
    <app-carousel></app-carousel>
    <app-carousel></app-carousel>
    <app-carousel></app-carousel>

    <app-footer></app-footer>
  </div>

</template>

<script>
  import AppHeader from './components/pages/Header.vue';
  import AppFooter from './components/pages/Footer.vue';
  import AppCarousel from './components/ui/AppCarousel.vue';

  export default {
    name: 'app',
    components: {AppHeader,AppFooter,AppCarousel},
    data () {
      return {
        msg: 'Food~',
        image: {
          source: require('./assets/logo.png'),
          alternate_text : '다시만난세계 푸드트럭'
        }
      }
    },
    methods:{
      changeHeading(){
        this.msg = '다시 만난 세계'
      }
    }
  }
</script>


<style lang="sass">
$bg-color: skyblue
$fg-color: #fff

body 
  color: $fg-color
  background: $bg-color

#app
  width: 80%
  max-width: 1200px
  margin:
    left: auto
    right: auto

</style>
