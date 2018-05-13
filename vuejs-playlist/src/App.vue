<template>
  <div>
    <app-header></app-header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Ninjas from './components/Ninjas.vue'

export default {
  components: {
    'app-header': Header,
    'app-ninjas': Ninjas, 
    'app-footer': Footer
  },
  data () {
    return {
      ninjas: [
              {name: "Ant", speciality:"Dev Stuff", show: false},
              {name: "Ben", speciality:"Law", show: false},
              {name: "Joe", speciality:"Engineering", show: false},
              {name: "Dan", speciality:"Saving the World", show: false},
              {name: "Sam", speciality:"Aciton Man", show: false},
              {name: "Dylan", speciality:"Who the fuck is dylan", show: false},
          ]
    }
  }
}
</script>

<style>

</style>
