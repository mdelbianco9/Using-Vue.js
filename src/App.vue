<template>
  <div id="app">


    <div class="navbar has-shadow">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item">MockMeUp</a>

          <!-- the v-on toggles the hamburger, the v-bind binds the hamburger with the router-links below -->
          <button class="navbar-burger" v-on:click="toggleNav" v-bind:class="{ 'is-active':isActive }">
            <span></span>
            <span></span>
            <span></span>
          </button>
        </div>

        

        <div class="navbar-end navbar-menu" v-bind:class="{ 'is-active':isActive }">

          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="Faq" class="navbar-item r-item">Features</router-link>
          <router-link to="Faq" class="navbar-item r-item">About</router-link>
          <router-link to="Faq" class="navbar-item r-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
                <a class="button is-primary is-outlined">
                  <span class="icon">
                    <i class="fa fa-download"></i>
                  </span>  
                  <span>Join Now</span>
                </a>
            </p>
          </div>
          
        </div>
      </div>
    </div>


    
    <!-- This is where the home and FAQ will reside -->
    <router-view></router-view>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>This is a- spiffy footer for you Mr. Bond</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-facebook"></i></a>
            <a class="icon" href="#"><i class="fa fa-twitter"></i></a>

          </div>
        </div>
      </div>
    </footer>

  </div>
</template>




<script>

export default {
  name: 'app',
  data: function () {
    return {
      isActive: false
    }
  },

  // this toggles between true and false for the isActive function. 

  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'


.navbar 
  background-color: #383838
  a:hover
    color: grey

.navbar-brand a
  color: #fff
  font-weight: bold


a.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem
  +mobile 
    color: grey
    &:hover 
      background-color: #F1F1F1

.navbar-burger
  background-color: #383838
  border: none
  color: #F1F1F1

footer 
  background-color: $primary !important
  color: #fff

  .icon 
    color: #fff
    margin-right: 20px

</style>
