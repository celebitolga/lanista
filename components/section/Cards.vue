<template>
  <div>
    <Card v-for="(card, index) in cards" :key="'card-'+index" :card="card" :choice="choice"/>
  </div>
</template>

<script>
import Card from '@/components/section/Card';

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
  },
}
</script>