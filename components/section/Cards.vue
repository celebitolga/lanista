<template>
  <div>
    <Card v-for="(card, index) in cards" :key="'card-'+index" :card="card" :choice="choice" class="cardShow"/>
    
    <swiper
      class="swiperShow"
      :slides-per-view="3"
      :space-between="50">
      <swiper-slide v-for="(card, index) in cards" :key="'card-'+index">
        <Card :card="card" :choice="choice" class="deneme"/>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import Card from '@/components/section/Card';

import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
import SwiperCore, { Navigation, Pagination, Scrollbar, A11y } from 'swiper';

SwiperCore.use([Navigation, Pagination, Scrollbar, A11y]);

export default {
  props: {
    cards: {
      type: Array,
      required: true,
    },
    choice: {
      type: Boolean,
      required: true,
    },
  },
  components: {
    Card,
    SwiperSlide,
    Swiper,
  },
  computed: {
   swiper () {
       return this.$refs.processSwiper.swiper // this.$refs: {}
   }
  },
  mounted () {
   return this.$refs.length // 1
  },
}
</script>

<style lang="scss" scoped>
.swiperShow {
  display: none;
}

.swiper-slide {
  width: 50% !important;
}

@media (max-width: 992px){

  .cardShow {
    display: none;
  }
  .swiperShow {
   display: block;
   width: 100%;
  }
}
@media (max-width: 768px){

}

@media (max-width: 576px){

}

@media (max-width: 320px){

}
</style>