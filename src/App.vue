<template>
  <div id="app">
      <div class="navbar navbar-default navbar-fixed-top scroll-me">
        <!-- pass scroll-me class above a tags to starts scrolling -->
        <div class="container">
            <div class="navbar-header">
                <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" href="#">
                    <img src="/dist/assets/img/logo.png"  alt="Naimul Ferdous"/>
                </a>
            </div>
            <div class="navbar-collapse collapse">
                <ul class="nav navbar-nav navbar-right">
                    <li><router-link to="/">Home</router-link></li>
                    <li><router-link to="/about">About</router-link></li>
                    <li><router-link to="/works">Works</router-link></li>
                    <li><router-link to="/blog">BLOG</router-link></li>
                    <li><router-link to="/contact">Contact</router-link></li>
                </ul>
            </div>

        </div>
    </div>
    <!-- NAVBAR END  -->
    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
import App from './App.vue'
import VueRouter from 'vue-router'
import Home from './pages/Home'
import About from './pages/About'
import Contact from './pages/Contact'
import Works from './pages/Works'
import Blog from './pages/Blog'
import Testimonial from './pages/Testimonial'


Vue.use(VueRouter)

const routes = [
  { path: '/', component: Home },
  { path: '/about', component: About },
  { path: '/contact', component: Contact },
  { path: '/works', component: Works },
  { path: '/blog', component: Blog },
  { path: '/testimonial', component: Testimonial }
]

const router = new VueRouter({
  routes: routes,
  mode: 'history'
})
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  router: router
}
</script>

<style>

</style>
