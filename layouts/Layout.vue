<template>
  <div>
    <Header />
    <Content />
    <Footer />
  </div>
</template> 

<script>
import Header from '@theme/components/Header.vue'
import Footer from '@theme/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
h1 {
    color: red;
}
</style>