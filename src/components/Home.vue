<template>
  <div class="home">
     <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-4"> {{ subheading }}</h2>
          </div>
          <a class="button is-large is-primary" id="learn">Learn More</a>
        </div>
      </div>
     </section>

     <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">

          <div class="column is-1 has-text-centered">
            <i class="fa fa-cog is-primary"></i>
          </div>

          <div class="column is-one-third-desktop">
            <p class="title"><strong>We provide superior logistics so your business can succeed in crazy world.</strong></p>
          </div>

          <div class="column">
            <p>Lorem Ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.</p>
          </div>
        </div>
      </div>

      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">"I thinks its an exelent tool for business. I cant survive without it."</p>
              <p class="subtitle">Gary Bungus</p>
            </div>
          </div>
        </div>
      

      
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">"I thinks its an exelent tool for business. I cant survive without it."</p>
              <p class="subtitle">Gary Bungus</p>
            </div>
          </div>
        </div>
      

      
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">"I thinks its an exelent tool for business. I cant survive without it."</p>
              <p class="subtitle">Gary Bungus</p>
            </div>
          </div>
        </div>
      </div>
    
     </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      heading: "Getting Practice with MockUps",
      subheading: "Lorem Ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups."
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'

.hero 
  background: url('../assets/hero.jpg')
  background-size: cover

  .title 
    color: #fff
    +mobile
      font-weight: bold
    +tablet
      font-weight: 2.5rem
    +desktop
      font-weight: 7rem
      margin-top: 2rem

h2 
  margin: 1.5rem 0 2rem 0 !important
  color: #fff

.fa-cog 
  font-size: 40px

#learn
  +desktop
    margin-bottom: 2rem

.pd
  +tablet
    padding: 2em 0
  +desktop
    padding: 2em 0

.title
  font-weight: 200;


</style>
