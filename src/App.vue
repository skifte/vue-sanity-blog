<template>
  <div class="app-wrapper">
    <header class="siteheader">
      <div class="container">
          <nav class="sitenav">
            <router-link :to="{ name: 'Home'}" :class="{'router-link-active': $route.name === 'SinglePost'}">
              <div class="svg-wrapper"> 
                <SVGairplane/> 
              </div>
              <span>Flyblogg</span>
            </router-link>
            <router-link :to="{ name: 'About'}">Om Anders Skifte</router-link>
        </nav>
      </div>
    </header>
    <main>
    <router-view :key="$route.fullPath" />
    </main>
  </div>
  <footer class="sitefooter">
    <div class="container">
      Flybloggen er laget med <a href="https://vuejs.org/">Vue.js</a> og <a href="https://www.sanity.io/">Sanity.io</a>. 
      Den kjører hos <a href="https://www.netlify.com/">Netlify</a>. Koden er på <a href="https://github.com/skifte/flyblogg-vue-sanity">Github</a>.
    </div>
  </footer>
</template>

<script>
import SVGairplane from './components/SVGairplane.vue'
export default {
  components: {
    SVGairplane
  }
}
</script>
