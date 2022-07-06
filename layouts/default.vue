<template>
  <div class="">
    <div class="container">
      <Navbar/>
      <Header/>
      <Nuxt />
      <About/>
      <div class="container">
        <div class="row">
          <Skill class="col-md-6"/>
          <Project class="col-md-6"  />
        </div>
      </div>
      <Mail/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Footer1 from '~/components/Footer.vue';
export default {
  name : 'Default',
  components: {
    Navbar: () => import("~/components/Navbar.vue"),
    Header: () => import("~/components/Header.vue"),
    About: () => import("~/components/About.vue"),
    Skill: () => import("~/components/Skill.vue"),
    Project: () => import("~/components/Project.vue"),
    Mail: () => import("~/components/Mail.vue"),
    Footer: () => import("~/components/Footer.vue"),
  }
}
</script>
