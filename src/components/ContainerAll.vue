<template>
  <div class="container">
    <TopMenu />
    <HeroTop />
    <AboutView />
    <ResumeView v-show="false" />
    <WorkView v-show="false" />
    <BlogView v-show="false" />
    <ContactView v-show="false" />
  </div>
</template>

<script>
import TopMenu from './TopMenu.vue'
import HeroTop from './HeroTop.vue'
import AboutView from '../views/AboutView.vue'
import ResumeView from '@/views/ResumeView.vue'
import WorkView from '@/views/WorkView.vue'
import BlogView from '@/views/BlogView.vue'
import ContactView from '@/views/ContactView.vue'
export default {
  name: 'ContainerAll',
  components: {
    TopMenu,
    AboutView,
    ResumeView,
    HeroTop,
    WorkView,
    BlogView,
    ContactView
  }
}
</script>

<style scoped>
@media (min-width: 561px) {
  .container {
    margin: 0 auto;
    padding: 0 1.5rem 0 10rem;
    max-width: 70rem;
    position: relative;
    z-index: 1;
  }
}

@media (min-width: 1200px) {
  .container {
    max-width: 1286px;
    max-height: 674px;
  }
}
</style>
