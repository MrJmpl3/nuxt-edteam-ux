<template lang="pug">
  header(:class="classHeader")
    div.ed-grid.cols-s-5.cols-l-4
      div.span-s-4.span-l-1.cross-center
        nuxt-link(to="/")
          slot(v-if="currentPage === 'Clase (video)'")
            img(src="/img/edteam-logo-alt.svg").main-logo
          slot(v-else)
            img(src="/img/edteam-ux-logo.svg").main-logo
      div.span-s-1.span-l-3.cross-center.main-end.header-links
        nav.main-menu#main-menu
          ul
            li
              a(href="https://ed.team" target="_blank") Ir a EDteam
            li
              a(href="https://cursos.ed.team" target="_blank") Ir a Plataforma de cursos
        .main-menu-toggle.to-l#main-menu-toggle
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
    currentPage: ''
  }),
  computed: {
    classHeader() {
      if (this.currentPage === 'Clase (video)') {
        return 'main-header--dark';
      } else {
        return 'main-header';
      }
    }
  }
};
</script>

<style scoped>
</style>
