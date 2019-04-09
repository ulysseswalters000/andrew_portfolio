<template lang="pug">
  div#aboutBlurb
    b-container.bg-info(fluid)
      b-container.pt-4.text-white
        h1.text-center.text-uppercase Meet Me
        b-row.mt-4.py-4
          b-col.mt-4(cols="12" md="6")
            b-img(thumbnail rounded="circle" src="../assets/images/headshot.png")
          b-col.mt-4(cols="12" md="6")
            h2.text-center.text-uppercase What I do
            b-nav.bg-secondary(fill)
              b-nav-item(@click="webDesign")
                p.text-light.mb-0 Web Design
              b-nav-item(@click="seo")
                p.text-light.mb-0 SEO
              b-nav-item(@click="content")
                p.text-light.mb-0 Content Generation
            b-card.no-rounded.text-left(
              bg-variant="dark"
              text-variant="white"
              img-src="https://images.unsplash.com/photo-1505852679233-d9fd70aff56d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
            )
              b-card-title {{ services.title }}
              b-card-sub-title {{ services.subTitle }}
              b-card-body {{ services.serviceData }}
        b-container.text-center.py-4.mt-4
          b-button(size="lg" @click="contact") Contact
</template>

<script>
export default {
  data() {
    return {
      services: {
        title: `Web Design`,
        subTitle: `Custom and CMS Solutions`,
        serviceData: `Using a few years knowledge in HTML, CSS, and
                    Javascript, I love to build beautiful and functional
                    websites. Currently, I am a huge fan of Vue.js which
                    is what this site is built with.`
      }
    };
  },
  methods: {
    webDesign() {
      this.services.title = `Web Design`
      this.services.subTitle = `Custom and CMS Solutions`
      this.services.serviceData = `Using a few years in knowledge in HTML, CSS, and
                          Javascript, I love to build beautiful and functional
                          websites. Currently, I am a huge fan of Vue.js which
                          is what this site is built with.`
    },
    seo() {
      this.services.title = `SEO`
      this.services.subTitle = `Search Engine Optimization`
      this.services.serviceData = `Search Engine Optimization Is the most important
                                   tool to get your website seen. I have served
                                   many businesses and helped them reach top
                                   google rankings for their keyword targets. I
                                   also have experience building links both on and
                                   off site.`
    },
    content() {
      this.services.title = `Content Generation`
      this.services.subTitle = `Optimized and engaging Prose`
      this.services.serviceData = `Content is king. In a constant battle for
                                   readership and users that drive sales, updating
                                   and generating new and engaging content is a must
                                   in the current digital world. I have ghost written
                                   many articles for my clients that have helped expand their
                                   client base and brought them more prosperity.`
    },
    contact() {
      this.$router.push('/contact')
    }
  }
}
</script>

<style lang="scss" scoped>
.small-text {
  font-size: .5rem;
}

.no-rounded {
  border-radius: 0 !important;
}
</style>
