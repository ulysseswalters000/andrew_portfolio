<template lang="pug">
  div#projects.bg-secondary
    b-container.py-4
      h1.my-4.py-4.text-center.text-white Current Clients
      b-row
        b-col.my-4(cols="12" md="6" lg="4" v-for="client in clients")
          b-card.position-relative.equal-height(
              bg-variant="primary"
              text-variant="white"
            )
            div.hovered.position-absolute
              div.overlay.position-absolute
                router-link.link(to="client.link") 
                  p Visit Site
            b-img(fluid :src="client.img" )
            b-card-title.my-2 {{ client.title }}
            b-card-subtitle.my-2 {{ client.subTitle }}
            b-card-body.my-2 {{ client.body }}
            i.fas.fa-arrow-right.float-right
            
          

</template>

<script>
export default {
  data(){
    return {
      clients: {
        rvaglass: {
          title: `RVA Glass LLC.`,
          subTitle: `Auto Glass Repair`,
          body: `RVA Glass LLC. had some trouble with their previous web hosting 
                 selling to a company that was not very customer service oriented.
                 My company was able to get Andrew's website back up and running 
                 the same day and have been working together to increase his 
                 online business ever since.`,
          link: `https://rvaglassrepair.com`,
          img: require(`../assets/images/rva_glass.jpg`)
        },
        neb: {
          title: `Never Enough Books`,
          subTitle: `Book Store &amp; E-commerce`,
          body: `Never Enough Books contacted my digital marketing business 
                 about helping their new location get more foot traffic as well 
                 as e-commerce sales.`,
          link: `https://neverenoughbooksva.com`,
          img: require(`../assets/images/NEB_logo.svg`)
        },
        cheuphoria: {
          title: `Cheuphoria`,
          subTitle: `Gourmet Charcuterie Catering`,
          body: `Cheuphoria is committed to providing gourmet charcuterie with 
                 impeccable service under a sustainable business model that 
                 supports local economy while generating living wages.`,
          link: `https://cheuphoriarva.com`,
          img: require(`../assets/images/Cheuphoria_Logo.jpg`)
        }
      }
    }
  },
  methods: {
    linkAway(link) {
      this.router.$push(link)
    }
  }
}
</script>

<style lang="scss" scoped>
.text-underline {
  text-decoration: underline;
}

.overlay {
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0);
  display: flex;
  align-items: center;
  text-transform: uppercase;
  visibility: hidden;
}

.hovered {
  width: 100%; height: 100%; color: black; top: 0; right: 0;
}
.hovered:hover > .overlay {
  background-color: rgba(10, 10, 10, .8);
  visibility: visible;
}

.link {
  display: flex;
  width: 100%;
  height: 100%;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: red;
}

.flex-grow {
  flex: 1;
}





</style>
