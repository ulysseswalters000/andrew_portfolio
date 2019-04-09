<template lang="pug">
  div.fixed-top
    nav
      b-navbar(toggleable="lg" type="dark" variant="dark")
        b-navbar-brand(href="/") AW
        
        b-navbar-toggle(target="nav-collapse")
        
        b-collapse#nav-collapse(is-nav)
          b-navbar-nav.ml-auto.color
            b-navbar-item
              router-link.p-2.d-block.link-style(to="/") Home
            b-navbar-item
              router-link.p-2.d-block.link-style(to="/about") About
            b-navbar-item
              router-link.p-2.d-block.link-style(to="/contact") Contact
            b-navbar-item
              router-link.p-2.d-block.link-style(to="/portfolio") Portfolio
    


</template>
//- Script
<script>
export default {
  name: "Navbar"
};
</script>

<style lang="scss" scoped>
.color {
  color: #fff;
}

.link-style {
  text-decoration: none;
  color: #fff;

  &:hover {
    background-color: #444;
    color: #000;
  }
}
</style>
