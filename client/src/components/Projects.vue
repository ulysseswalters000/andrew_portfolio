<template lang="pug">
  div#projects
    b-container.py-4.my-4
      h1.my-4.py-4.text-center Current Clients
      b-row
        b-col.my-4(cols="12" sm="6")
          b-card.mx-2(
              bg-variant="primary"
              text-variant="white"
            )
            b-img(thumbnail width="325px" fluid src="../assets/images/NEB_logo.svg" )
            b-card-title.my-2 Never Enough Books
            b-card-subtitle.my-2 Book Store
            b-card-body.my-2
              router-link.pr-1.text-white.text-underline(to="https://neverenoughbooksva.com") Never Enough Books
              | contacted my digital marketing business
              router-link.text-white.px-1.text-underline(to="https://zendodigital.com") Zendo Digital
              | about helping their new location get more foot traffic as well as e-commerce sales.
        b-col.my-4(cols="12" sm="6")
          b-card.mx-2(
              bg-variant="primary"
              text-variant="white"
            )
            b-img(thumbnail width="325px" fluid src="../assets/images/rva_glass.jpg" )
            b-card-title.my-2 RVA Glass LLC.
            b-card-subtitle.my-2 Auto Glass Repair
            b-card-body.my-2
              router-link.px-1.text-white.text-underline(to="https://rvaglassrepair.com") RVA Glass LLC.
              | had some trouble with their previous web hosting selling to a company that was not very customer service oriented.
              | My company was able to get Andrew's website back up and running the same day and have been working together
              | to increase his online business ever since.
        b-col.my-4(cols="12" sm="6")
          b-card.mx-2(
              bg-variant="primary"
              text-variant="white"
            )
            b-img(thumbnail width="325px" fluid src="../assets/images/NEB_logo.svg" )

</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.text-underline {
  text-decoration: underline;
}
</style>
