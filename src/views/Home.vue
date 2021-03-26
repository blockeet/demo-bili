<template>
  <div class="home">
    <header>
      <nav-user></nav-user>
      <nav-banner></nav-banner>
      <div class="content-warp">
        <primary-menu></primary-menu>
      </div>
    </header>
    <main>
      main
      <aside>
        nav
      </aside>
    </main>
    <footer>
      footer
    </footer>
  </div>
</template>

<script>
import NavUser from '@/components/NavUser.vue'
import NavBanner from '@/components/Banner.vue'
import PrimaryMenu from '@/components/PrimaryMenu.vue'

export default {
  name: 'Home',
  components: {
    NavUser,
    NavBanner,
    PrimaryMenu
  }
}
</script>

<style lang="scss">
  .content-warp {
    width: 1630px;
    margin: 0 auto;
  }
</style>
