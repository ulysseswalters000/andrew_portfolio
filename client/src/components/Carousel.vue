<template lang="pug">
  div#carousel
    b-carousel(
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    )
      b-carousel-slide(
        caption="Web Development"
        text="Stunning, modern websites at affordable prices."
        img-src="https://images.unsplash.com/photo-1536257104079-aa99c6460a5a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
      )
      b-carousel-slide(
        caption="SEO"
        text="Search Engine Optimization strategies to advance your business on the web."
        img-src="https://images.unsplash.com/photo-1515961896317-adf9e14bdcc0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
      )
      b-carousel-slide(
        caption="Content Generation"
        text="Ghost Writer for optimized blog posts as well as content for website generation."
        img-src="https://images.unsplash.com/photo-1505852679233-d9fd70aff56d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
      )
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    }
  }
};
</script>

<style lang="scss" scoped></style>
