<template>
  <footer class="Footer container">

    <FooterBanner />
    
    <FooterFloor />

  </footer>
</template>

<script>
import FooterBanner from '@/components/footer/FooterBanner';
import FooterFloor from '@/components/footer/FooterFloor';

export default {
  components: {
    FooterBanner,
    FooterFloor,
  },
}
</script>

<style lang="scss" scoped>
.Footer {
  
}
</style>