<template>
  <div class="home">
    <header>
      <nav-user></nav-user>
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

export default {
  name: 'Home',
  components: {
    NavUser
  }
}
</script>
