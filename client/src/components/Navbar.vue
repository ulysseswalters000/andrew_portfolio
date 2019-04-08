<template lang="pug">
  div
    nav.navbar.navbar-expand-lg.navbar-dark.bg-dark
      router-link.navbar-brand(to="/") AW
      button.navbar-toggler(type="button" data-toggle="collapse" data-target="#navbarContent" aria-controls="navbarContent")
        span.navbar-toggler-icon
      div#navbarContent.collapse.navbar-collapse
        div.navbar-nav.ml-auto
          router-link.nav-item.nav-link(to="/") Home
            span.sr-only (current)
          router-link.nav-item.nav-link(to="/About") About
          router-link.nav-item.nav-link(to="/Contact") Contact
          router-link.nav-item.nav-link(to="/Portfolio") Portfolio


</template>
//- Script
<script>
export default {
  name: "Navbar"
}
</script>

<style lang="scss" scoped>
a {

}

</style>
