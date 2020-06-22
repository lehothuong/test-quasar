<template>
  <div class="bg-main introContent">
    <q-carousel
      animated
      v-model="slide"
      swipeable
      navigation
      infinite
    >
      <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg"></q-carousel-slide>
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg"></q-carousel-slide>
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg"></q-carousel-slide>
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg"></q-carousel-slide>
    </q-carousel>
    <div class="introFooter">
        <q-btn class="btnStart" @click.prevent="goToLoveTree" label="Bắt đầu" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Intro',
  data () {
    return {
      slide: 1
    }
  },
  mounted () {

  },
  methods: {
    goToLoveTree () {
      if (window.ReactNativeWebView) {
        window.ReactNativeWebView.postMessage('LOVETREE')
      }
    }
  }
}
</script>
