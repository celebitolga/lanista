<template>
  <div>
    <Hero />

    <FirstSection />

    <SecondSection />
  </div>
</template>

<script>
import Hero from '@/components/hero/Hero';
import FirstSection from '@/components/section/FirstSection';
import SecondSection from '@/components/section/SecondSection';

export default {
  components: {
    Hero,
    FirstSection,
    SecondSection,
  },
}
</script>

<style>

</style>
